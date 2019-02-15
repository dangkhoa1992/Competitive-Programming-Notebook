
## Struct sort
```C++
struct Object {
    int index;
    ll value;
    ll weight;
};
vector<Object> objects;

// Sort value/weight decreasing
sort(objects.begin(), objects.end(), 
    [](const Object &a, const Object &b) 
        {return a.value*b.weight > b.value*a.weight;});
```

## Struct sort - Priority
```C++
struct Object {
    int index;
    ll firstPrior;
    ll secondPrior;
};
vector<Object> objects;

// Sort 1st prior decreasing - 2nd prior increasing
sort(objects.begin(), objects.end(), 
    [](const Object &a, const Object &b) 
        {return a.secondPrior < b.secondPrior;});

stable_sort(objects.begin(), objects.end(), 
    [](const Object &a, const Object &b) 
        {return a.firstPrior > b.firstPrior;});
```