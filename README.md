# Mencari-Frekuensi

    #include<iostream>
    #include<conio.h>
    using namespace std;
    int main()
    {
    int data[10];
    int jumlah,tmp,N;
    cout<<"masukkan banyak data:";cin>>N;
    for(int i=0;i<N;i++)
    {
        cout<<"Data ke-"<<i+1<<":";cin>>data[i];
    }
    cout<<"data diurutkan :";
    for(int h=0;h<N;h++)
    {
        for(int i=h+1;i<N;i++)
        {
            if(data[h]>data[i])
            {
                tmp=data[i];
                data[i]=data[h];
                data[h]=tmp;
            }
        }
        cout<<data[h]<<" ";
    }
    cout<<"\nBanyak kemunculan data :"<<endl;
    for(int h=0;h<N;h++)
    {
        jumlah=0;
        for(int i=0;i<N;i++)
        {
            if(data[h]==data[i])
                jumlah++;
        }
        if(data[h]!=data[h-1])
            cout<<data[h]<<":"<<jumlah<<endl;
    }
    getch();
    }

## Hasilnya

![img](https://github.com/ernico27/Mencari-Frekuensi/blob/master/frekuensi.png?raw=true)
