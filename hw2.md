<h1>HW2</h1>
<table>
  <tr>
      <td>
        <img src="hw2.GIF">
      </td>
  </tr>
  

```swift
import SwiftUI
// future for HW2

struct HandView: View{
    var imgName:String
    var body: some View
    {
        VStack{
            
            Image(imgName)
                .resizable()
                .aspectRatio( contentMode:.fit)
                .frame(height: 100 ,alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
        }
        .frame(minWidth: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealWidth: /*@START_MENU_TOKEN@*/100/*@END_MENU_TOKEN@*/, maxWidth: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, minHeight: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealHeight: /*@START_MENU_TOKEN@*/100/*@END_MENU_TOKEN@*/, maxHeight: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
    }
}

struct ContentView: View {
    @State var URcount:Int = -1
    @State var count:Int = -1
    @State var hand :String = "猜猜拳"
    @State var result :String = "猜猜拳"
    @State var pic :String = "猜"
    var body: some View {
        
        Text(String("Result：\(result)")) //only String Type
            .font(.system(size: 50))
        
        if(pic == "猜"){
            Image("\(pic)")
                .resizable()
                .aspectRatio(contentMode: .fit)
                .foregroundColor(.accentColor)
            
            //.clipShape(/*@START_MENU_TOKEN@*/Circle()/*@END_MENU_TOKEN@*/, style: /*@START_MENU_TOKEN@*/FillStyle()/*@END_MENU_TOKEN@*/)
                .frame(width:500, height: 300, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
        }
        else{
            Image("\(pic)")
            // .frame(width:500, height: 300, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                .font(.system(size: 50))
            //.resizable()
                .aspectRatio(contentMode: .fit)
                .foregroundColor(.accentColor)
                .clipShape(/*@START_MENU_TOKEN@*/Circle()/*@END_MENU_TOKEN@*/, style: /*@START_MENU_TOKEN@*/FillStyle()/*@END_MENU_TOKEN@*/)
                .frame(width:500, height: 300, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
        }
        //     .font(.system(size: 30))
        HStack{
            Button(action: {
                var asd = Int(arc4random())
                asd = asd % 3
                count = asd
                pic = ""
                if count == 0{
                    pic = "剪刀"
                    hand = "剪刀"}
                else if count == 1{
                    hand = "石頭"
                    pic = "石頭"
                }
                else{ hand = "布"
                    pic = "布"
                }
                if hand == "布" {result = "Lose"}
                else if hand == "剪刀" {result = "Win"}
                else {result = "Tie"}
                print (count)   
            }, label: {
                //Text("石頭").foregroundColor(/*@START_MENU_TOKEN@*/.blue/*@END_MENU_TOKEN@*/)
                //
                //.frame(width:500, height: 300, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                  //  .font(.system(size: 30))
                    //.resizable()
                //.aspectRatio(contentMode: .fit)
                //.foregroundColor(.accentColor)
               //     .clipShape(/*@START_MENU_TOKEN@*/Circle()/*@END_MENU_TOKEN@*/, style: /*@START_MENU_TOKEN@*/FillStyle()/*@END_MENU_TOKEN@*/)
                Image("A")
                //.frame(width:500, height: 300, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                   // .font(.system(size: 30))
                    .resizable()
                    .aspectRatio(contentMode: .fit)
                    .foregroundColor(.accentColor)
                    .clipShape(/*@START_MENU_TOKEN@*/Circle()/*@END_MENU_TOKEN@*/, style: /*@START_MENU_TOKEN@*/FillStyle()/*@END_MENU_TOKEN@*/)
                    .frame(minWidth: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealWidth: /*@START_MENU_TOKEN@*/100/*@END_MENU_TOKEN@*/, maxWidth: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, minHeight: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealHeight: /*@START_MENU_TOKEN@*/100/*@END_MENU_TOKEN@*/, maxHeight: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
            }
                   
            )
            
            Button(action: {
                var asd = Int(arc4random())
                asd = asd % 3
                count = asd
                pic = ""
                if count == 0{
                    pic = "剪刀"
                    hand = "剪刀"}
                else if count == 1{
                    hand = "石頭"
                    pic = "石頭"
                }
                else{ hand = "布"
                    pic = "布"
                }
                if hand == "石頭" {result = "Lose"}
                else if hand == "布" {result = "Win"}
                else {result = "Tie"}
                
                print (count)   
            }, label: {
                Image("C")
                    //.frame(width:500, height: 300, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                    //.font(.system(size: 30))
                    .resizable()
                    .aspectRatio(contentMode: .fit)
                    .foregroundColor(.accentColor)
                    .clipShape(/*@START_MENU_TOKEN@*/Circle()/*@END_MENU_TOKEN@*/, style: /*@START_MENU_TOKEN@*/FillStyle()/*@END_MENU_TOKEN@*/)
                
                    .frame(minWidth: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealWidth: /*@START_MENU_TOKEN@*/100/*@END_MENU_TOKEN@*/, maxWidth: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, minHeight: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealHeight: /*@START_MENU_TOKEN@*/100/*@END_MENU_TOKEN@*/, maxHeight: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                // Text("剪刀").foregroundColor(/*@START_MENU_TOKEN@*/.blue/*@END_MENU_TOKEN@*/)
            })
            
            Button(action: {
                var asd = Int(arc4random())
                asd = asd % 3
                count = asd
                pic = ""
                
                if count == 0{
                    pic = "剪刀"
                    hand = "剪刀"}
                else if count == 1{
                    hand = "石頭"
                    pic = "石頭"
                }
                else{ hand = "布"
                    pic = "布"
                }
                if hand == "剪刀" {result = "Lose"}
                else if hand == "石頭" {result = "Win"}
                else {result = "Tie"}
                
                print (count)   
            }, label: {
                Image("B")
                //.frame(width:500, height: 300, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
                    //.font(.system(size: 30))
                    .resizable()
                    .aspectRatio(contentMode: .fit)
                    .foregroundColor(.accentColor)
                    .clipShape(/*@START_MENU_TOKEN@*/Circle()/*@END_MENU_TOKEN@*/, style: /*@START_MENU_TOKEN@*/FillStyle()/*@END_MENU_TOKEN@*/)
                    .frame(minWidth: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealWidth: /*@START_MENU_TOKEN@*/100/*@END_MENU_TOKEN@*/, maxWidth: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, minHeight: /*@START_MENU_TOKEN@*/0/*@END_MENU_TOKEN@*/, idealHeight: /*@START_MENU_TOKEN@*/100/*@END_MENU_TOKEN@*/, maxHeight: /*@START_MENU_TOKEN@*/.infinity/*@END_MENU_TOKEN@*/, alignment: /*@START_MENU_TOKEN@*/.center/*@END_MENU_TOKEN@*/)
            }
                   
            )
            
            
            
          
        }
        Button(action: {
            count = -1
            URcount = -1
            print (count)
            hand = "猜猜拳"
            result =  "猜猜拳"
            pic = "猜"
        }, label: {
            Text("Reset")
        })
    }
}

  
```
</table>
