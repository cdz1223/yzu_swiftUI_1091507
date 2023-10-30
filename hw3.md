<h1>HW1</h1>
<table>
  <tr>
      <td>
        <img src="hw3.jpg">
      </td>
  </tr>
  

```swift
import SwiftUI
// future for HW3
struct nameView: View{
    var body: some View{
        VStack(alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/, spacing: 2) {
            Text("1091507的模型櫃").font(/*@START_MENU_TOKEN@*/.title/*@END_MENU_TOKEN@*/)
        }
        
    }
}

struct HandView: View{
    var imgName:String
    var tit:String
    var body: some View{
        ZStack{
            VStack{
                
                Image(imgName)
                    .resizable()
                    .aspectRatio( contentMode:.fit)
                    .frame(width:200 ,height: 120,alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                    .frame(minWidth: 0, idealWidth: 500, maxWidth: .infinity, minHeight: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealHeight: 200, maxHeight: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                
            }
            Text(tit)
                .font(.system(size:10))
                .foregroundColor(.yellow)
                .padding(.all,5)
                .background(Color.black)
                .opacity(0.7)
                .offset(x:0,y:50)
                
        }
    }
}
struct ContentView: View {
    var body: some View {
        nameView()
        HStack{
            HandView(imgName: "Godzilla", tit: "Mecha Godzilla")
            HandView(imgName: "Buddha",tit: "Buddah")
            HandView(imgName: "V01",tit: "nu Gundam")
            
}
        HStack{
            HandView(imgName: "Moto",tit: "GSX-S150")
        }
        HStack{
            HandView(imgName: "Zheng",tit: "Z")
            HandView(imgName: "V02",tit:"Nu-02")
            //HandView(imgName: "Bird",tit:"Bird")
            
        }
        HStack{
            HandView(imgName: "Wing",tit: "Wing Gundam")
            HandView(imgName: "Eva02",tit:"Eva02")
            HandView(imgName: "Bird",tit:"Bird")
            
        }
        
    }
}

  
```
</table>
