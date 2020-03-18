
# Java Code Standards

Readability is rule of thumb.


### Stack parameters:

// RECOMMEND

```
public View onCreateView(@NonNull LayoutInflater inflater,
                         @Nullable ViewGroup container,
                         @Nullable Bundle savedInstanceState) {
    return LayoutInflater
            .from(getContext())
            .inflate(R.layout.seeding_form, container, false);
}
```
// NOT RECOMMEND

```
public View onCreateView(@NonNull LayoutInflater inflater, @Nullable ViewGroup container, @Nullable Bundle savedInstanceState) {
  return LayoutInflater.from(getContext()).inflate(R.layout.seeding_form, container, false);
}
```

## Naming Conventions:

* Any naming should have <= 3 words

### ENUM
```
enum Day {
    SUNDAY, MONDAY, TUESDAY,
    WEDNESDAY, THURSDAY, FRIDAY,
    SATURDAY
}

setDayType(MONDAY)     // RIGHT
setVisibility(GONE)    // RIGHT

setDayType(Day.MONDAY) // AVOID
```

### BOOLEAN

```
isSelected   // RIGHT

setSelected  // AVOID
selected     // AVOID
```
```
hasHeader      // RIGHT

withHeader     // AVOID
containHeader  // AVOID
```

### LIST
```
List<Employee> employees;    // RIGHT

List<Employee> employeeList; // AVOID
```

### FUNCTION
```
void setEmployee(Employee employee)()  // RIGHT

void set(Employee e)()                 // AVOID
void set(Employee employee)()          // AVOID
```

##### ON CLICK LISTENER
```
void onAcceptButton() // RIGHT

void acceptPressed()  // AVOID
```

##### FOR-LOOP (-)
```
for (Company company : companies) {}       // RIGHT

for (int i = 0; i < companies.size(); i++) // AVOID
```

### IF ELSE / Ternary Operator

// RECOMMEND

```
String greeting = isMorning
    ? "Good Morning"
    : "Good Night";
```

// NOT RECOMMEND
```
String greeting = "";
if (isMorning) {
    greeting = "Good Morning";
} else {
    greeting = "Good Night";
};
```

### SWITCH CASE

// RECOMMEND

```
// Empty space in between cases.
// Include every case.
// Watch out for fall through

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

// RECOMMEND

```
<plurals name="employees_size">
    <item quantity="one">%d employee</item>
    <item quantity="other">%d employees</item>
</plurals>


setText(getResources().getQuantityString(
    R.plurals.employees_size,
    employees.size(),
    employees.size()));

```
// NOT RECOMMEND

```
setText(employees.size()
    ? "1 employee"
    : employees.size() + " employees")

```

### ID
```
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
