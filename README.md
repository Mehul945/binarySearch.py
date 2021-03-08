# binarySearch.py
















def sort(list):
    for i in range(len(list)-1):
        if i==len(list)-1:
            pass
        elif list[i]>list[i+1]:
            temp=list[i]
            list[i]=list[i+1]
            list[i+1]=temp

    return list
def search(list,num):
    list=sort(list)
    l=0
    r=len(list)
    while 1:
        mid=(l+r)//2
        if num==list[mid]:
            print(f"{num} is present in list")
            break
        elif num>list[mid]:
            l=mid
        elif num<list[mid]:
            r=mid
        if l==r-1:
            print(f"{num} not in list")
            break
