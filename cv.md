# Tsimafei Zykau

* Email: zikovtm@gmail.com
* Phone: +375 (29) 892-67-82
* Telegram: @dobry_kum
* LinkedIn: https://www.linkedin.com/in/timofey-z-b8439b11b/

## Summary

I always interested in Information Technology and developing applications for mobile phones. So right now my main goal is to expand my skills at programming and learn how to write applications for Apple systems. One day I wish to successfully complete iOS Dev course by RSSchool and EPAM and get an offer for a job as a Junior iOS Developer

## Skills

* HTML, CSS
* Vanilla JS
* Python 3
* Swift
* CoreData
* Grand Central Dispatch
* MVC, MVVM
* C, C++
* Pascal, Delphi
* MySQL, SQLite
* Git
* Object-oriented programming

## Code Examples

[Technical Task with News.org API](https://github.com/dobryKum/NewsApp)

And small code example of controller that gets photo from NASA API

```
//
//  PhotoInfoController.swift
//  SpacePhoto
//
//  Created by Tsimafei Zykau on 8/9/19.
//  Copyright © 2019 Timofey Zykov. All rights reserved.
//

import Foundation

class PhotoInfoController {
    func fetchPhotoInfo(completion: @escaping (PhotoInfo?) -> Void) {
        let baseUrl = URL(string: "https://api.nasa.gov/planetary/apod")!
        
        let query: [String: String] = [
            "api_key": "DEMO_KEY",
            "date": "2010-07-15"
        ]
        let url = baseUrl.withQueries(query)!
        let task = URLSession.shared.dataTask(with: url) { (data, response, error) in
            let jsonDecoder = JSONDecoder()
            if let data = data,
                let photoInfo = try? jsonDecoder.decode(PhotoInfo.self, from: data) {
                completion(photoInfo)
            } else {
                print("Something went wrong.")
                completion(nil)
            }
        
        }
        task.resume()
    }
}
```

## Experience

1. [Small Experience at HackerRank](https://www.hackerrank.com/dobry_kum)
2. Worked with Swift language for a few months
3. Right now working with AVR Microcontrollers(*C*) and Raspberry Pi(*Python*) in university projects

## Education

* Belarussian State University of Informatics and Radioelectronics, Faculty of Computer-Aided Design, Programming Mobile Systems, Second year
* Fully read and completed all tasks from book [App Development with Swift by Apple Education](https://books.apple.com/ru/book/app-development-with-swift/id1219117996)
Right now started to read a book Effective Objective-C 2.0 by Galloway Matt.

## Engilsh

Studied English language at High School, for about a year with tutor and first year in University. Right now I can read books and watch movies in English, but I will understand only 70-80 percent of them. My speaking skill is also getting weaker
