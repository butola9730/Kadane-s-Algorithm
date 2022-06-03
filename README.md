# Kadane-s-Algorithm
#include <bits/stdc++.h>
using namespace std;

int main()
{
  int n;
  cin>>n;

  int arr[n];

  for(int i=0; i<n; i++)
    cin>>arr[i];

  int maxsum = INTMIN, currsum =0;

  for(int i=0; i<n; i++){

   currsum += arr[i];

   if(maxsum < currsum)
     maxsum = currsum;

   if(currsum < 0)
     currsum = 0;

  }

  cout<<maxsum;

  return 0;
}
