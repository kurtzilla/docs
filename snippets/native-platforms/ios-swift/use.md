```swift
// HomeViewController.swift

Auth0
    .webAuth()
    .start {
        switch $0 {
        case .failure(let error):
            // Handle the error
            print("Error: \(error)")
        case .success(let credentials):
            // Do something with credentials e.g.: save them.
            // Auth0 will automatically dismiss the hosted login page
            print("Credentials: \(credentials)")
        }
}
```
