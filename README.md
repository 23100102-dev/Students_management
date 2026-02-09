8
Transformation into tabular representation in reverse order:

Algorithm:

cin>>N;

k=-1;
while (N>=1)
{
k++;
b[k]=N%10;
N=N/10;
}

for(i=0; i<=k; i++)
cout<<b[i]<<" ";

Transformation into tabular representation in direct order:

Algorithm:

cin>>N;
k=0;
L=N;
while (L>=1)
{
	L=L/10;
	k++;
}
k--;
m=k;
while (N>=1)
{
b[k]=N%10;
N=N/10;
k--;
}

for(i=0; i<=m; i++)
cout<<b[i]<<" ";

Transformation of the tabular representation of numbers into ordinary representation:

a=a1a2a3...an , 

a=a1·10n¬¬¬¬-1 + a2·10n-2 + a3·10n-3 + ... + an-1·10 + an

Algorithm:

cin>>n;
for(i=0; i<n; i++)
cin>>b[i];

a=0;
r=1;
for(i=0; i<n; i++)
{
	a=a+b[i]*r;
	r=r*10;
}
cout<<a;
cout<<endl;

Transformation of the tabular representation of numbers into ordinary representation (Horner’s scheme):



Algorithm:
cin>>n;
for(i=0; i<n; i++)
cin>>b[i];
a=0;
for(i=0; i<n; i++)
	a=a*10+b[i];
cout<<a;








9

Long numbers summation:


k=max(n,m)+1;
for(i=0; i<k; i++)
	{c[i]=a[i]+b[i]+c[i];
	 if (c[i]>=10)
	   {c[i]=c[i]%10;
	    c[i+1]=c[i+1]+1;}
    }
k--;
if(c[k]==0)
  k--;
for(i=k; i>=0; i--)
	cout<<c[i]<<” “;

Long numbers subtraction:

for(i=0; i<n; i++)
	{c[i]=a[i]-b[i]+c[i];
	 if (c[i]<0)
	   {c[i]=c[i]+10;
	    c[i+1]--;}
    }
   
while(c[n]==0)
  n--;
for(i=n; i>=0; i--)
	cout<<c[i]<<” “;

Long numbers multiplication:

k=n+m;

for(i=0; i<m; i++)
  for(j=0; j<n; j++)
   c[i+j]=a[j]*b[i]+c[i+j];
   
   for(i=0; i<k-1; i++)
	{c[i+1]=c[i+1]+c[i]/10;
	 c[i]=c[i]%10; }
	 
 while(c[k]==0)
  k--;
for(i=k; i>=0; i--)
	cout<<c[i]<<” “;











10

Recursion

Factorial:
N!=1*2*3*4*5…*N
0!=1
Recurrent relation:
N!=N*(N-1)!

Iterative algorithm:
cin>>n;
Fact=1;
For(i=2; i<=n; i++)
Fact=Fact*i;
cout<<Fact;

Recursive algorithm:
int n, k;

int Fact(int n)
{
if(n==1)
  return 1;
    else
      return n*Fact(n-1);
}
int main()

{
cin>>n;
k=Fact(n);
cout<<k;
}

11
Recursion 

Recursive and cyclic algorithms of finding the nth member of Fibonacci sequence and difference between them:

Recurrence realtion:
F(i) = F(i-1) + F(i-2)

Cyclic algorithm:
With indices:
cin>>n;
F[1]=1;
F[2]=1;
for(i=3; i<=n; i++)
F[i] = F[i-1] + F[i-2];
cout<<F[n];

Without indices:
a=1;
b=1;
for (i=3; i<=n; i++)
{
c=a+b;
a=b;
b=c;
}
Recursive algorithm:
int n, k;
int Fib (int n)
{
if (n==1 || n==2)
  return 1;
    else
      return Fib(n-1) + Fib(n-2);
}
int main ()
{
cin>>n;
k= Fib(n-1) + Fib(n-2);
cout<<k;
}

12

Data Structures

QUEUE:         FIFO (First in First out)


Initialization of a new queue

QUEUE_INIT
{
Head=0;
Tail=0;
}


Insertion of new element in the queue

ENQUEUE (x)
{
Q[Head]=x;
Head++;
}


Deletion of element from a queue

DEQUEUE
{
Tail++;
Return Q[Tail-1];
}

QUEUE_EMPTY
{
If (Tail<Head)
Return false;
Else
Return true;
}

12


Data Structures

STACK:         FILO (First in Last out)

Initialization of a new stack

STACK_INIT
{
Top=-1;
}

Insertion of new element in a stack

PUSH (x)
{
Top++;
S[Top]=x;
}

Deletion of element from a stack

POP
{
Top--;
Return S[Top+1];
}

STACK_EMPTY
{
If (Top>=0)
Return false;
Else
Return true;
}






  
