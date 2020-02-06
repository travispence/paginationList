# paginationList

[![pub package](https://img.shields.io/badge/pub-0.0.1-blueviolet.svg)](https://pub.dev/packages/paginationList)<br>
A Pagination Library for Flutter (with Web Support).

### How to Use
just add below in pubspec.yaml 
```
paginationList: ^0.0.1
```
```
import 'package:paginationList/paginationList.dart';
```
Demo Code:
```
    PaginationList<User>(
        separatorWidget: Container(
          height: 0.5,
          color: Colors.black,
        ),
        itemBuilder: (BuildContext context, User user) {
          return ListTile(
            title:
                Text(user.prefix + " " + user.firstName + " " + user.lastName),
            subtitle: Text(user.designation),
            leading: IconButton(
              icon: Icon(Icons.person_outline),
              onPressed: () => null,
            ),
            onTap: () => print(user.designation),
            trailing: Icon(
              Icons.call,
              color: Colors.green,
            ),
          );
        },
        pageFetch: pageFetch,
        onError: (dynamic error) => Center(
          child: Text('Something Went Wrong'),
        ),
        ...
        onEmpty: Center(
          child: Text('Empty List'),
        ),
      ),
```
<br>
<img align="middle" src="https://user-images.githubusercontent.com/52414184/73923273-9d803f00-48f0-11ea-9d1c-2e66a8517eeb.gif" width=270 height=550>
<br>

### For more info:
Email: ssvekariya11@gmail.com