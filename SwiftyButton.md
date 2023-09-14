# Simple SwiftButton


```` ruby
struct ContentView: View {
  
  @State var swiftyColor: Color = .red
  @State var swiftyOpacity: Double = 0.7
  
    var body: some View {
      VStack {
        ColorPicker("Swifty Color", selection: $swiftyColor)
        Slider(value: $swiftyOpacity, in: 0...3)
          .accentColor(swiftyColor)
        Image(systemName: "swift")
          .resizable()
          .scaledToFit()
          .foregroundColor(.white)
          .opacity(swiftyOpacity)
          .background(swiftyColor)
          .cornerRadius(50)
      }
      .padding()
    }
}

struct ContentView_Previews: PreviewProvider {
    static var previews: some View {
        ContentView()
    }
}
````


![alt text](https://github.com/Poulsen89/SwiftCode.md/blob/090aaaaba3ed61273a045a17af258e69b8a43576/Ska%CC%88rmavbild%202023-09-14%20kl.%2013.24.20.png)
