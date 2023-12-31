# KXR.LTI Back-end Software 2023-2024

This repository stores all active code used by the
**Knights Experimental Rocketry** (***KXR***)'s
**Launch & Testing Infrastructure** (***LTI***)
Back-end Software Development team for the 2023-2024 season.

###### README by KXR.LTI Back-end Software Development Team Lead [Will Serface](https://discord.com/users/609211773303652372).

______

## Projects

The following list is a description of all active and completed projects
in this repository. Each project listed here has a more detailed description
included with the file `README.md` in its respective directory.

- Control Panel Switch & LED Controller `status: in ideation`
  > The Control Panel will be to provide Ground Support crew with an easy and
  > reliable way of interfacing with the DAQ and telemetry system. This will
  > include a series of switches, buttons, and LEDs that enable both information
  > and control to any current or future KXR flight computer or motor test stand.
- Data Acquisition & Telemetry `status: in ideation`
  > The Data Acquisition (DAQ) and Telemetry system is vital for monitoring and
  > controlling the state of any rockets or test stands. It must be able to
  > recieve data from the Embedded Design team's FPGA implementation to both
  > record and send live data. This will involve decoding a binary stream to
  > relevant data, sending the processed data to long-term storage, and
  > creating or implementing an API that allows the secure transfer of data
  > and control for and the Front-end team's telemetry system.

___

## Organization & Documentation Best Practices

### GitHub & Branches

The completed "Production" version of code, specifically for launches and
static fire tests, will be stored in the
[`main`](https://github.com/KXR-UCF/BackendSoftware24/tree/main) branch,
while each task or feature in active development will be kept in its own
individually named branch, and after review, shall be merged back into
[`main`](https://github.com/KXR-UCF/BackendSoftware24/tree/main)
and archived. This will allow the Production code to only have a single
feature change made at a time, which will allow the team to easily identify 
the source of any unforseen incompatibilities between versions.

Please include a concise summary and add more detail in the description
when adding a commit to the repository. If working on multiple tasks simultaneously,
please be mindful of which branch you target when committing changes.

### Code

For the sake of readability for both current and future members of ***KXR.LTI***,
any code added by the team to any project in this repository is expected be
well-written. This includes easily read formatting, good organization,
and frequent comments describing the purpose of each series of statements.

For example, below is my ideal way of writing comments in *C*.
While there is no specified format of comments, please be generous with the
amount of quality documentation we have for ourselves and our future team members.

```C
// PREPROCESSOR DIRECTIVES
#include <stdio.h> // Standard Input/Output Library
#define pi 3.14 // Used for calculating area of a circle

// FUNCTION DECLARATIONS
double area(double r); // Calculates the area of a circle of radius r
double volume(double r, double h); // Calculates the area of radius r and height h

// MAIN FUNCTION
int main() {
    // Function Variables
    double radius, height; // User inputs for calculating measurements
    
    // Get user input for radius
    printf("Enter the radius:\n");
    scanf("%lf", &radius);
    
    // Get user input for height
    printf("Enter the height:\n");
    scanf("%lf", &height);
    
    // Computation and Output
    printf("Volume = %f unit(s)^3.\n", volume(radius, height));
    
    // Successful Exit
    return 0;
}

// FUNCTION DEFINITIONS
double area(double r) {
    return (pi * r * r); // A = pi*r^2
}

double volume(double r, double h) {
    return (area(r)*h); // V = A*h
}
```

