## Введение
Диаграммы выполнены в 
- [PlantUML](https://plantuml.com/) 
- [two.js](https://two.js.org/) 
 
# Информатика

> "Язык программирования — это формальная знаковая система, предназначенная для описания алгоритмов вычислений таким образом, чтобы они были понятны и человеку, и машине."

> Полнота по Тьюрингу — характеристика исполнителя (множества вычисляющих элементов) в теории вычислимости, означающая возможность реализовать на нём любую вычислимую функцию. Другими словами, для каждой вычислимой функции существует вычисляющий её элемент (например, машина Тьюринга) или программа для исполнителя, а все функции, вычисляемые множеством вычислителей, являются вычислимыми функциями (возможно, при некотором кодировании входных и выходных данных).

(Turing-completeness, TC) — это свойство системы при некотором простом представлении ввода и вывода реализовать любую вычислимую функцию.

#### Критерии Тьюринг-полноты

Если на языке программирования можно реализовать машину Тьюринга, то такой язык Тьюринг-полон, и наоборот. Возможность реализации машины Тьюринга на конкретном языке программирования можно грубо описать как перечень требований, которым этот язык должен для этого удовлетворять:

- Конечность (нет бесконечных символьных множеств и пр.).
- Фиксированное описание (формальность [^1]).
- Всегда достаточный объём доступной памяти — в идеале здесь имеется в виду неограниченная память, однако физические рамки не позволяют сделать память ЭВМ бесконечной, поэтому она просто должна быть "*always big enough*".
- Неограниченность времени выполнения — любая программа должна иметь возможность работать до тех пор, пока не завершится.
- Возможность функциональной композиции (вызов одной функции из другой, рекурсия).
- Наличие циклов _while_ с прерыванием или эквивалентных им конструкций.
- Возможность останавливать выполнение (halt) или каким-то образом подавать сигнал о результатах выполнения.
- Представление множества натуральных чисел, понятие нуля и следующего числа. Возможны другие подобные системы.
- Поддержка входных и выходных данных (I/O), причём без формальных ограничений в объёме. Очевидно, что если любая программа, написанная на каком-то языке программирования, принимает на вход не более фиксированного _n_ бит данных и возвращает не более _n_ бит, этот язык не может быть Тьюринг-полным.

#### Граф изображающий реализацию основных языков программирования:

<img src="https://raw.githubusercontent.com/IPOLIPOL/Informatika/main/visualizations/LanguageGraph-page1.svg" alt="Diagram" width="100%"/>

#### Граф изображающий основыне определения и их взаимосвязь:

<img src="https://raw.githubusercontent.com/IPOLIPOL/Informatika/main/visualizations/LanguageGraph-page2.svg" alt="Diagram" width="100%"/>

#### Пример выполнения программы на языке С:

<img src="https://raw.githubusercontent.com/IPOLIPOL/Informatika/main/visualizations/C_program_execution.svg" alt="Diagram" width="100%"/>

#### Объектно-ориентированный подход

<img src="https://raw.githubusercontent.com/IPOLIPOL/Informatika/main/visualizations/OOP_hex.svg" alt="Diagram" width="100%"/>

##### Interfaces an Strong Typing

OOP insists that classes specify the API (application programming interface) or simply ```interface```, that their objects present to other objects. This interface is specified as a class type definition and a collection of methods for this type, with the arguments for each method being of specified types. This specification is enforced by the complier or runtime system, which requires that the types of parameters that are actually passed to methods rigidly confomr with the type specified in the interface. This requirement is known as a ```strong typing```.

##### Inheritance and Polymorphism

OOP provides ways of reusing code in software system. 

#### Computer networks

OSI (Open Systems Interconnection) Model  

| Layer        | Definition                                                                                               | Protocols                         |
|--------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------|
| Application  | Provides network services to user applications                                                            | HTTP, FTP, SMTP, DNS              |
| Presentation | Translates data formats, encryption and compression                                                       | TLS, SSL, MIME                    |
| Session      | Manages sessions and connection control between hosts. Dialog between application programs.               | RPC, NetBIOS                      |
| Transport    | Lowest layer required to the programs for moving the data                                                 | TCP, UDP                          |
| Network      | Routing of data between devices. (Equivalent to Internet layer in TCP/IP model)                           | IP, ICMP, OSPF, BGP               |
| Data Link    | Error-prone physical circuit. Transmission of data frames                                                 | Ethernet, PPP, MAC                |
| Physical     | Electrical/optical/radio signaling over physical circuit. Transmission of bit streams                     | Cables, Wi-Fi, Ethernet, Bluetooth|


- OSI model created by ISO in 1984, described in ISO 7498.  
- OSI model defines 7 functional layers with the intent to make each layer as independent as possible from each other.  
- Three top three layers are related to the application programs services.  
- Four bottom layers are concerned with the network itself, providing the general data transport services.  
- Data frame - the unit of data.  
- Packet - the unit of data.  
- IP - Internet Protocol.  
- TCP - Transmission Control Protocol.  

[^1]: [Википедия — Формальный язык](https://ru.wikipedia.org/wiki/%D0%A4%D0%BE%D1%80%D0%BC%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B9_%D1%8F%D0%B7%D1%8B%D0%BA) 
