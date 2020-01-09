# Change-Date-format-to-another-format
This can change the date from one format to any other desired format

Source :- https://stackoverflow.com/a/56255649/12189609


## Extension to use :-

```swift
extension String {
func formattedDate(inputFormat: String, outputFormat: String) -> String {
    let inputFormatter = DateFormatter()
    inputFormatter.dateFormat = inputFormat

    if let date = inputFormatter.date(from: self) {
        let outputFormatter = DateFormatter()
        outputFormatter.dateFormat = outputFormat
        return outputFormatter.string(from: date)
    } else {
        return self  // If the string is not in the correct format, we return it without formatting
    }
}

```

## How to use :- 

```swift
labelDate.text = strDate.formattedDate(inputFormat: "MM/dd/yyyy", outputFormat: "dd, MMM yyyy")
```
