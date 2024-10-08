# Unbound Report
Unbound Report is a powerful tool designed to extract and visualize test suite data from Robot Framework's output.xml file. The report is generated as a comprehensive HTML document, offering a clear and detailed view of your test execution. The report can be generated via the command line or by importing the module into your Python code.

## Features
* Extract Detailed Test Data: Capture information about test suites, test cases, keywords, and nested structures like loops from the Robot Framework's output.xml file.
* Generate Interactive HTML Reports: Produce an HTML report with detailed sections, including graphical statistics, suite/test case details, and defect tracking.
* Command-Line Interface and Module Import: Flexibility to generate reports using a simple command-line interface or by importing the module into your own scripts.

## Report Structure
The generated Unbound Report consists of three main sections:  
View Report : [Unbound Report](https://prasad0275.github.io/unbound-report/demo-unbound-report.html)
### Overview Section:
Provides graphical representations of test execution statistics, including pass/fail rates, duration, and other key metrics.
Helps in understanding the overall performance and health of the test execution at a glance.
### Suites Section:
Displays a list of all test suites along with their respective test cases.
For each test case, it shows the associated keywords, their status, and execution time.
Includes detailed information about setup/teardown actions and any nested keywords or loops.
### Defects Section:
Focuses on the test cases that failed during execution.
Highlights common errors and allows for quick identification of problematic areas in the test suites.


## Installation
Install the package using pip:
```
pip install unbound-report
```
## Usage
### Command-Line Interface
You can generate the Unbound Report from the command line with the following command:

```
unboundreport -o /path/to/output.xml -s /path/to/save/
```

#### options
* -h, --help : show this help message and exit
*  -v, --version : Version
*  -o OUTPUT, --output OUTPUT : Path to the input output.xml file
*  -l LOG, --log LOG : Path to the input log.html file
*  -s SAVE_PATH, --save-path SAVE_PATH : Path to save the processed file

#### Example
```
unboundreport -o output.xml -s ./reports
```
This command will parse the output.xml file and generate an HTML report named unbound-report.html.

### Using as a Module
You can also generate the report by importing the module into your Python script:
```
from unbound_report.generate_report import generate_report

generate_report(output_file='output.xml',log_file='log.html', save_path='demo.html')
```
#### Example
```
from unbound_report.generate_report import generate_report

generate_report(output_file='output.xml',log_file='log.html', save_path='report.html')
```
This script will achieve the same result as the command-line example.

## Development
To contribute to this project:

1. Clone the repository.
2. Install dependencies.
3. Implement new features or fix bugs.
4. Submit a pull request.

## Contributing
Contributions are welcome! If you find any issues or have suggestions for new features, please create an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.



