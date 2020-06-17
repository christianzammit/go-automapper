# go-automapper

[![GoDoc](https://godoc.org/github.com/PeteProgrammer/go-automapper?status.svg)](https://godoc.org/github.com/PeteProgrammer/go-automapper)

<p>Go-automapper can automatically map data between different types with identically named fields in GO. Useful for initializing DTO types from build in data.</p>

<h4>time.Time support</h4>
<p>Due to using the <a href="https://golang.org/pkg/reflect/" target="_blank">Reflect</a> package to map source and destination types, it has a limitation when it comes to types were the initialization of the type uses private functionalities (such as <a href="https://golang.org/pkg/time/" target="_blank">time</a>), which is not supported by the Reflect package.</p>

<p>However, due to frequent use of time.Time as variable type, the latest release allows the mapping of time.Time to string. That is if for example a database entitiy has a CreatedDate of type time.Time (or *time.Time), a DTO wanting to expose CreatedDate must include CreatedDate of type string (or *string).</p>
