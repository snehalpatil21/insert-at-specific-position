# insert-at-specific-position
//insert at specific position.
#include<iostream.h>
#include<conio.h>
class traverse
{
int arr[50], i, elem, pos, tot;
public:
  void get();
  void insert();
    void display();
};
void traverse::get()
{ 
    cout<<"Enter the Size for Array: ";
    cin>>tot;
    cout<<"Enter "<<tot<<" Array Elements: ";
    for(i=0; i<tot; i++)
        cin>>arr[i];
}
void traverse::insert()
{
	cout<<"\nEnter Element to Insert: ";
    cin>>elem;
    cout<<"At What Position ? ";
    cin>>pos;
    for(i=tot; i>=pos; i--)
        arr[i] = arr[i-1];
    arr[i] = elem;
    tot++;
}
void traverse::display()
{
cout<<"\nThe New Array is:\n";
    for(i=0; i<tot; i++)
        cout<<arr[i]<<"  ";
    cout<<endl;
}
int main()
{
	 traverse t;
	 t.get();
	 t.insert();
	 t.display();
	 return 0;
}
