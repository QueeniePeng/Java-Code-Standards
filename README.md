
# Java Code Standards

Readability is rule of thumb.


## Stack parameters:

```
// RIGHT

public View onCreateView(@NonNull LayoutInflater inflater,
                         @Nullable ViewGroup container,
                         @Nullable Bundle savedInstanceState) {
    return LayoutInflater
            .from(getContext())
            .inflate(R.layout.seeding_form, container, false);
}
```
```
// AVOID

public View onCreateView(@NonNull LayoutInflater inflater, @Nullable ViewGroup container, @Nullable Bundle savedInstanceState) {
  return LayoutInflater.from(getContext()).inflate(R.layout.seeding_form, container, false);
}
```

## Naming Conventions:

* Any naming should have <= 3 words


### BOOLEAN

```
isSelected  // RIGHT

setSelected // AVOID
selected     
```
```
hasHeader   // RIGHT

withHeader  // AVOID
containHeader  
```

### LIST
```
List<Employee> employees;    // RIGHT

List<Employee> employeeList; // AVOID
```

### FUNCTION

#### 0. PARAMETERS
```
void setEmployee(Employee employee)() // RIGHT

void set(Employee e)()                // AVOID
void set(Employee employee)()
```

#### 1. ON CLICK LISTENER
```
void onAcceptButton()// RIGHT

void acceptPressed() // AVOID
```

#### 2. FOR-LOOP
```
for (Company company : companies) {}       // RIGHT

for (int i = 0; i < companies.size(); i++) // AVOID
```

### IF ELSE / Ternary Operator

```
String greeting = isMorning // RIGHT
    ? "Good Morning"
    : "Good Night";
```

```
String greeting = "";      // AVOID
if (isMorning) {
    greeting = "Good Morning";
} else {
    greeting = "Good Night";
};
```

### SWITCH CASE

1. Empty space in between cases.
2. Include every case.


```
// RIGHT

int getCalories() {    

    switch (breakfast) {
        case BACON:
            return 140;

        case EGG:   
            return 70;

        default:
            return 0;
    }
}
```

## RESOURCES

### STRINGS


```
// RIGHT

<plurals name="employees_size">
    <item quantity="one">%d employee</item>
    <item quantity="other">%d employees</item>
</plurals>


setText(getResources().getQuantityString(
    R.plurals.employees_size,
    employees.size(),
    employees.size()));

```
```
// AVOID

setText(employees.size()
    ? "1 employee"
    : employees.size() + " employees")

```

### ID

```
// RIGHT

TextView:  text_
ImageView: image_
Button:    button_
```
```
<ImageView
    android:id="@+id/image_profile"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content" />

<menu>
    <item
        android:id="@+id/menu_done"
        android:title="Done" />
```








&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
&nbsp;
