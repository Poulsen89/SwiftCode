import SwiftUI

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
