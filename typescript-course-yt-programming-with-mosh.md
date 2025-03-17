# TypeScript Course - YT / Programming with Mosh

# TypeScript Nedir?

TypeScript, Microsoft tarafından geliştirilen ve JavaScript'in bir üst kümesi olan, statik tür sistemine sahip bir programlama dilidir. TypeScript, JavaScript'in tüm özelliklerini içerir ve ek olarak tür denetimi, nesne yönelimli programlama (OOP) desteği ve gelişmiş IDE entegrasyonu gibi avantajlar sunar. TypeScript kodları, tarayıcılar ve Node.js gibi JavaScript çalıştırma ortamlarında kullanılabilmesi için JavaScript'e derlenir.

## Static ve Dinamik Kodlama Arasındaki Fark

Kodlama paradigmaları açısından iki temel tür vardır: **statik (static) kodlama** ve **dinamik (dynamic) kodlama**.

### Statik Kodlama

- Değişkenlerin veri türleri derleme aşamasında belirlenir ve sabittir.
- Derleyici, hataları kod çalıştırılmadan önce tespit edebilir.
- Örnek diller: TypeScript, Java, C#, C++.
- Daha güvenlidir ve büyük ölçekli projeler için uygundur.
- Performans açısından avantajlıdır, çünkü tür denetimi çalışma zamanında değil, derleme aşamasında yapılır.

### Dinamik Kodlama

- Değişkenlerin türleri çalışma zamanında belirlenir.
- Hata tespiti genellikle çalışma zamanında olur.
- Örnek diller: JavaScript, Python, Ruby.
- Daha esnektir ve hızlı geliştirme sağlar.
- Küçük projeler için genellikle daha uygundur.

TypeScript, statik tür sistemine sahip olduğu için yazılım geliştirme sürecinde daha fazla güvenlik sağlar ve ölçeklenebilir projeler için avantaj sunar.

## TypeScript'in Avantajları

### 1\. **Statik Tür Denetimi**

TypeScript, kodun derleme aşamasında hataları yakalayarak çalışma zamanı hatalarını en aza indirir. Bu, özellikle büyük projelerde hata ayıklamayı kolaylaştırır.

### 2\. **Daha İyi IDE Desteği**

TypeScript, popüler kod editörleri ve IDE'ler ile güçlü bir entegrasyona sahiptir. Otomatik tamamlama, hata ayıklama ve geliştirme sürecini hızlandıran araçlar sunar.

### 3\. **Güçlü Nesne Yönelimli Programlama (OOP) Desteği**

Sınıflar, arayüzler, soyutlamalar ve modüller gibi OOP konseptleri, TypeScript’te güçlü bir şekilde desteklenir.

### 4\. **Daha Anlaşılır ve Bakımı Kolay Kod**

Tür sisteminin sağladığı açıklık sayesinde kodun okunabilirliği ve sürdürülebilirliği artar. Büyük ekiplerde çalışırken, farklı geliştiricilerin yazdığı kodun anlaşılmasını kolaylaştırır.

### 5\. **JavaScript ile Geriye Dönük Uyumlu**

Mevcut JavaScript projelerine TypeScript eklenebilir ve TypeScript kodları standart JavaScript'e derlendiği için herhangi bir tarayıcı veya Node.js ortamında çalışabilir.

### 6\. **Geniş Kapsamlı Ekosistem ve Topluluk Desteği**

TypeScript, Microsoft tarafından aktif olarak geliştirilmekte olup büyük bir topluluk tarafından desteklenmektedir. Bu sayede geniş bir kütüphane ve framework desteği mevcuttur.

### 7\. **Modern JavaScript Özelliklerini Destekler**

TypeScript, ES6 ve daha yeni JavaScript özelliklerini kullanma imkanı sunar. Böylece eski tarayıcılara ve platformlara yönelik kodlar üretirken modern sözdizimini kullanabilirsiniz.

TypeScript, özellikle büyük ölçekli projeler, ekip çalışması gerektiren projeler ve hata oranını minimize etmek isteyen geliştiriciler için ideal bir çözümdür. Dinamik JavaScript ortamında çalışan ancak statik kodlama avantajlarından faydalanmak isteyenler için güçlü bir alternatiftir.

* * *

## TypeScript Kurulumu

TypeScript ile geliştirme yapmak için aşağıdaki adımları takip ederek kurulum yapabilirsiniz.

### 1\. **Node.js ve npm’in Yüklü Olduğundan Emin Olun**

Öncelikle, Node.js ve npm’in sisteminizde kurulu olup olmadığını kontrol edin:

```
node -v
npm -v
```

Eğer kurulu değilse, [Node.js’in resmi sitesinden](https://nodejs.org/) yükleyebilirsiniz.

### 2\. **Yeni Bir Proje Başlatın**

Yeni bir TypeScript projesi oluşturmak için aşağıdaki komutu çalıştırarak bir proje dizini oluşturun:

```
mkdir my-ts-project && cd my-ts-project
```

Ardından, bir `package.json` dosyası oluşturmak için:

```
npm init -y
```

Bu komut, varsayılan değerlerle bir `package.json` dosyası oluşturur.

### 3\. **TypeScript’i Yükleyin**

TypeScript’i geliştirme bağımlılığı olarak eklemek için aşağıdaki komutu kullanın:

```
npm install --save-dev typescript
```

Bu işlem tamamlandıktan sonra, TypeScript’i çalıştırmak için kullanılacak `tsc` (TypeScript Compiler) komutu projenizde kullanılabilir hale gelir.

### 4\. **tsconfig.json Dosyası Oluşturun**

TypeScript’in proje ayarlarını belirlemek için aşağıdaki komutu çalıştırarak bir `tsconfig.json` dosyası oluşturabilirsiniz:

```
npx tsc --init
```

Bu dosya, TypeScript’in nasıl derleneceğini belirten ayarları içerir.

### 5\. **Vite Kullanarak TypeScript Projesi Başlatma**

Vite ile hızlı bir TypeScript projesi oluşturmak için aşağıdaki komutu çalıştırabilirsiniz:

```
npm create vite@latest my-ts-app --template vanilla-ts
```

Bu komut, TypeScript ile çalışan bir Vite projesi oluşturacaktır.

Ardından proje dizinine girin:

```
cd my-ts-app
```

Bağımlılıkları yükleyin:

```
npm install
```

Ve geliştirme sunucusunu başlatın:

```
npm run dev
```

Böylece TypeScript destekli bir Vite projesi çalıştırılmış olur.

* * *

# **TypeScript Veri Tipleri**

### **1\. Number**

TypeScript'te tüm sayılar number türündedir.

```
let age: number = 25;
let price: number = 99.99;
let hex: number = 0xff;
let binary: number = 0b1010;
let octal: number = 0o744;
```

### **2\. String**

Metinsel ifadeleri temsil eder.

```
let firstName: string = "John";
let lastName: string = 'Doe';
let greeting: string = `Hello, ${firstName}!`;
```

### **3\. Boolean**

true veya false değerlerini alır.

```
let isActive: boolean = true;
let hasPermission: boolean = false;
```

### **4\. Undefined**

Bir değişken tanımlandığında ancak değer atanmadığında undefined olur. Eğer programın ileriki safhalarında değişkene veri atanması söz konusu ise undefined veri tipi kullanılır. Null ile arasındaki fark budur.

```
let notDefined: undefined;
```

### **5\. Null**

Boş bir değeri temsil eder.

```
let emptyValue: null = null;
```

### **6\. Void**

Bir fonksiyonun değer döndürmediğini belirtir.

```
function logMessage(): void {
  console.log("This function returns nothing.");
}
```

### **7\. Never**

Hiçbir değeri temsil etmez. Örneğin, bir fonksiyon hata fırlattığında veya sonsuz döngüye girdiğinde never türü kullanılır.

```
function throwError(message: string): never {
  throw new Error(message);
}
```

* * *

## TypeScript'te Array ve Tuple Kullanımı

### **Array (Dizi) Kullanımı**

Array’ler TypeScript'te birden fazla değeri tutmak için kullanılır. Bütün array itemlerinin aynı veri tipine sahip olma zorunluluğu yoktur ancak hepsinin aynı olması kullanım rahatlığı açısından daha iyidir. Örneğin array çok tipli olursa seçili bir indekse işlem yapılamk isteneceği zaman oto-öneri seçeneği çalışmayacaktır çünkü indeksin hangi veri tipi olduğunu bilmeyecektir. Ancak array tek tipli olursa oto-öneri arraydeki bütün itemlerin aynı veri tipindne olduğunu bildiğinden öneri verebilecektir.

```
let arr1: number[] = [1, 2];
```

Bu, sadece `number` türünde değerler içeren bir dizidir.

```
let arr2: number[][] = [[1], [2]];
```

Bu, `number` türünden elemanlar içeren çok boyutlu bir dizidir.

```
let arr3 = [1, 2, 3, 'hello']; // (string | number)[]
```

Burada TypeScript, dizinin hem `string` hem de `number` türlerini içerebileceğini anlar.

### **Tuple Kullanımı**

Tuple, belirli türlerde sabit uzunluktaki dizilerdir. Veri tipi tanımlamasında kullanılan listedeki element sayısı ve tipi, değişkenin alacağı değerin yapısını temsil eder. Değer, bu tanımla aynı olmak zorundadır.

```
let tup1: [number, number] = [1, 2];
```

Bu, sadece `number, number` formatındaki iki elemandan oluşur.

```
let tup2: [string, number] = ['', 2];
```

Burada ilk eleman `string`, ikinci eleman `number` olmalıdır.

```
let tup3: [string, number][] = [['1', 2], ['1', 2]];
```

Bu, her elemanı `[string, number]` türünde olan bir dizi oluşturur.

```
let tup4: [string, number][][] = [[['1', 2], ['1', 2]]];
```

Burada ise, `tup3`'ten farklı olarak çift boyutlu bir tuple dizisi tanımlanmıştır.

* * *

### **Literal Types (Sabit Değerli Türler)**

Literal türler, bir değişkenin sadece belirli değerleri almasını sağlar. Bu, hata olasılığını azaltır ve kodun daha anlaşılır olmasını sağlar.

```
let lit1: "1" | "2" | "3" | "4" | "5";
lit1 = "hello" // Yanlış
lit1 = "3" // Doğru
```

Yukarıdaki örnekte `lit1` değişkeni yalnızca "1", "2", "3", "4" veya "5" değerlerini alabilir. Eğer başka bir değer atanırsa, TypeScript hata verecektir.

```
let lit2: true;
lit2 = false // Yanlış
lit2 = true // Doğru
```

Burada `lit2` değişkeni yalnızca `true` değerini kabul edebilir. `false` atanırsa TypeScript hata verecektir.

### **Enum Kullanımı**

Enum (numaralandırma) türleri, belirli sabit değerleri daha okunaklı hale getirmek ve gruplamak için kullanılır.

#### **Sayısal Enum**

```
enum Size {
    Small = 100,
    Medium,
    Large
}

let size: Size = Size.Small;
```

Burada `Size` adında bir enum oluşturulmuştur. `Small` değeri `100` olarak tanımlanmış, `Medium` ve `Large` ise otomatik olarak `101` ve `102` değerlerini almıştır.

#### **String Enum**

```
enum Team {
    Ts = "Ts",
    Bjk = "Bjk",
    Gs = "Gs",
    Fb = "Fb"
}

let favTeam: Team = Team.Ts;
```

Bu örnekte, `Team` adlı enum sadece belirli string değerleri içerebilir. `favTeam` değişkeni `Team.Ts` olarak tanımlanmıştır ve yalnızca `"Ts"`, `"Bjk"`, `"Gs"` veya `"Fb"` değerlerini alabilir.

Enum’lar, kodun okunabilirliğini artırarak `magic number` veya `magic string` hatalarını önler.

* * *

### Opsiyonel Tanımlama (Optional Chaining)

```
let arr = [{name: "Ali"}]
let el = arr.pop()?.name;
```

Yukarıdaki kodda, `arr.pop()?.name` ifadesi kullanılıyor. `pop()` işlemi, dizinin son elemanını kaldırır ve döndürür. Ancak, eğer dizi boşsa `undefined` dönecektir. `?.` (optional chaining) operatörü, `undefined` veya `null` değer dönmesi durumunda bir hata almadan `el` değişkenini `undefined` olarak atamamızı sağlar.

Örnek:

```
let arr: {name: string}[] = [];
let el = arr.pop()?.name; // undefined, çünkü dizi boş
```

### Kesin Tanımlama (Non-null Assertion)

```
let arr1 = [{name: "Ali"}]
let el1 = arr1.pop()!.name;
```

Burada `!` operatörü (non-null assertion) kullanılmıştır. `pop()` işlemi sonucu `undefined` dönebilir, ancak `!` operatörü derleyiciye `pop()` işleminin asla `undefined` olmayacağını belirtir. Eğer dizi gerçekten boşsa ve `pop()` `undefined`döndürürse, `undefined.name` hatası alırız.

Örnek:

```
let arr1: {name: string}[] = [];
let el1 = arr1.pop()!.name; // Runtime error: Cannot read properties of undefined (reading 'name')
```

Bu yüzden, `!` operatörünü dikkatli kullanmak gerekir. Eğer bir dizinin boş olup olmadığını bilmiyorsak, `?.` (optional chaining) kullanmak daha güvenlidir

* * *

# TypeScript'te Fonksiyonlar

TypeScript'te fonksiyon tanımlarken parametrelerin ve dönüş değerinin türlerini belirlemek mümkündür. Bu, kodun okunabilirliğini ve hata yakalama sürecini iyileştirir.

## Temel Fonksiyon Tanımlama

```
function add(a: number, b: number): number {
    return a + b;
}
```

Yukarıdaki `add` fonksiyonu iki `number` parametre alır ve bir `number` döndürür. Dönüş türü belirtilmezse TypeScript, dönen değeri otomatik olarak çıkarım yapabilir. Ancak, özellikle karmaşık fonksiyonlarda dönüş türünü açıkça belirtmek iyi bir uygulamadır.

## Birden Fazla Veri Tipi Döndüren Fonksiyonlar

```
function add1(a: number, b: number): string | number {
    if (a === 0) {
        return "invalid";
    }
    return a + b;
}
```

Bu fonksiyon ya bir `number` ya da bir `string` döndürebilir. TypeScript’te birden fazla dönüş tipi belirtmek için `|` operatörü kullanılır. Eğer dönüş türü belirtilmezse TypeScript otomatik olarak tahmin etmeye çalışır, ancak açıkça tanımlamak kodun daha anlaşılır olmasını sağlar.

## Opsiyonel Parametreler

```
function subtract(a: number, b: number, c?: number): number {
    if (c) {
        return a - b - c;
    } else {
        return a - b;
    }
}
```

Bir parametrenin zorunlu olmaması için `?` operatörü kullanılır. Burada `c` parametresi opsiyoneldir, yani çağırırken bu parametreyi vermek zorunlu değildir.

Örnek Kullanım:

```
subtract(10, 5); // 5 döndürür
subtract(10, 5, 2); // 3 döndürür
```

## Fonksiyonları Parametre Olarak Kullanma

```
function callAddition(add: (a: number, b: number) => number, a: number, b: number) {
    console.log(add(a, b));
}
```

Bu fonksiyon, bir başka fonksiyonu parametre olarak alır. `add` fonksiyonu, iki `number` alıp bir `number` döndüren bir fonksiyon olarak tanımlanmıştır.

Örnek Kullanım:

```
callAddition(add, 3, 4); // 7 yazdırır
```

## Daha Karmaşık Fonksiyon Kullanımı

```
function mul(num1: number, num2: number): number {
    return num1 * num2;
}

function div(num1: number, num2: number): number {
    return num1 / num2;
}

function applyFuncs(funcs: ((a: number, b: number) => number)[], values: [number, number][]) {
    let results = [];

    for (let i = 0; i < funcs.length; i++) {
        let args = values[i];
        let result: number = funcs[i](args[0], args[1]);
        results.push(result);
    }

    return results;
}
```

Bu kodda:

- `applyFuncs` fonksiyonu, birden fazla fonksiyonu (`mul`, `div` gibi) ve argümanları içeren bir dizi alır.
- `funcs` dizisi, her elemanı iki `number` parametre alan ve bir `number` döndüren fonksiyonlardan oluşur.
- `values` dizisi, ikili sayı grupları içeren bir dizi olarak tanımlanmıştır.
- `applyFuncs`, her fonksiyonu ilgili argümanlarla çalıştırıp sonucu `results` dizisine ekler.

Örnek Kullanım:

```
const results = applyFuncs([mul, div], [[6, 3], [10, 2]]);
console.log(results); // [18, 5]
```

* * *

TypeScript'te fonksiyonlara birden fazla parametre geçmek için rest parametreleri kullanılabilir. Rest parametreleri, belirtilen türdeki elemanların bir dizisini alır:

```
function getString(...items: string[]) {
    return items.join(", ");
}
```

Burada `getString` fonksiyonu, bir veya birden fazla `string` parametresi alabilir ve bunları birleştirerek döndürür.

### Overloaded Fonksiyonlar

Farklı veri tipleriyle çağrılabilen bir fonksiyon oluşturmak için fonksiyon overloading kullanılabilir. Aşağıdaki gibi bir tanım yapılır:

```
function getLength(name: string): number;
function getLength(name: string[]): number;
function getLength(nameOrNames: unknown): number {
    if (typeof nameOrNames === "string") {
        return nameOrNames.length;
    } else if (Array.isArray(nameOrNames)) {
        return nameOrNames.length;
    }
    return 0;
}
```

Bu örnekte:

- Eğer parametre `string` ise, string'in uzunluğunu döndürür.
- Eğer parametre `string[]` yani string dizisi ise, dizinin uzunluğunu döndürür.
- Eğer parametre farklı bir türde ise, `0` döndürür.

Bu yapı sayesinde, fonksiyon çağrıldığında TypeScript hangi overload'un kullanılacağını belirleyebilir.

* * *

## Interface Kullanımı

TypeScript'te `interface`, nesne tiplerini tanımlamak için kullanılır. Bir nesnenin hangi özelliklere sahip olması gerektiğini belirlemek için kullanılır.

### Interface Tanımlama

Aşağıdaki örnekte bir `Product` arayüzü tanımlanmıştır:

```
interface Product {
    id: number;
    name: string;
    description?: string; // Opsiyonel alan
    price: number;
}

function getProduct(product: Product): Product {
    return {
        id: 123,
        name: "hello",
        price: 45
    };
}
```

Burada `Product` arayüzü, bir ürünün sahip olması gereken özellikleri belirtir. `description` özelliği opsiyoneldir (`?` ile belirtilmiştir), yani bu alan olmadan da `Product` nesnesi oluşturulabilir.

### Interface ile Nesne Tanımlama

Bir `Person` arayüzü aşağıdaki gibi tanımlanabilir:

```
interface Person {
    name: string;
    surname: string;
    age: number;
    firstLanguage?: string; // Opsiyonel alan
}

const user1: Person = {
    name: "Ahmet",
    surname: "Aslan",
    age: 24
};
```

Burada `user1` nesnesi `Person` arayüzüne uygun olarak tanımlanmıştır.

### Interface Miras Alma (Extending Interfaces)

TypeScript'te `interface`ler diğer `interface`lerden miras alabilir. Bu sayede mevcut bir interface'i genişletmek mümkündür.

```
interface Employee extends Person {
    employeeId: number;
    returnId: () => void;
}

const employee1: Employee = {
    employeeId: 8234902,
    returnId: () => console.log(employee1.employeeId),
    name: "Alparslan",
    surname: "Demir",
    age: 38
};
```

Burada `Employee` arayüzü, `Person` arayüzünü genişletmektedir. Yani `Employee`, `Person`'dan gelen tüm özellikleri içermektedir ve ek olarak `employeeId` ve `returnId` gibi yeni özellikler kazanmıştır.

Bu yapı, TypeScript'te esnek ve ölçeklenebilir nesne tipleri oluşturmayı sağlar.

* * *

## **Classes**

**Classes**, nesne tabanlı programlamada (OOP) temel yapı taşlarından biridir. JavaScript’te sınıflar, nesnelerin özelliklerini ve davranışlarını tanımlamak için kullanılan bir şablondur. Sınıflar, bir nesnenin **özellikleri (properties)** ve **metotları (methods)** üzerinde işlem yapmanıza olanak tanır.

Sınıflar, bir nesne yaratıldığında, nesnenin belirli davranışlarını ve verilerini tutar. Her sınıf, **constructor (yapıcı)** fonksiyonu ile başlatılır. Bu fonksiyon, sınıfın her örneği oluşturulduğunda çalışır ve genellikle nesnenin ilk değerlerini ayarlamak için kullanılır.

### **Temel Sınıf Tanımlaması**

JavaScript’teki sınıf yapısını inceleyelim:

```
class Animal {
    protected name: string;

    constructor(name: string){
        this.name = name
    }

    getName() {
        return this.name
    }
}
```

Bu örnekte, **Animal** adında bir sınıf tanımlanmıştır. **protected** erişim belirleyicisi ile name özelliği korunmuş ve sadece bu sınıfın içinde ve ondan türetilen sınıflarda erişilebilecek şekilde tanımlanmıştır. **constructor** metodu sınıfın örneği oluşturulurken çalışır ve name özelliğini başlatır. **getName** metodu ise name değerini döndürmek için kullanılır.

### **Inheritance (Kalıtım)**

JavaScript’te sınıflar, kalıtım yoluyla diğer sınıflardan türeyebilir. Bu, bir sınıfın başka bir sınıfın tüm özelliklerini ve metotlarını devralmasını sağlar. Kalıtım, yeniden kullanılabilir kod yazımını kolaylaştırır.

Bir sınıfı kalıtımla türetmek için extends anahtar kelimesi kullanılır. Aşağıda **Dog** sınıfı, **Animal** sınıfından türetilmiştir:

```
class Dog extends Animal {
    family: string;

    constructor(species: string, family: string) {
        super(species) // Animal sınıfının constructor'ını çağırır
        this.family = family
    }

    getNamee() {
        console.log(this.name)
    }
}
```

Bu örnekte, **Dog** sınıfı **Animal** sınıfından türetilmiştir. **super(species)** ifadesi, üst sınıfın (Animal) constructor metodunu çağırır ve name özelliğini başlatır. Dog sınıfı ayrıca **family** adında bir özellik tanımlar ve **getNamee** adında bir metot içerir. Bu metod, name özelliğini konsola yazdırır.

### **Erişim Belirleyiciler**

Sınıflarda kullanılan erişim belirleyiciler, nesnenin özelliklerine ve metotlarına erişimi kontrol eder. Bu erişim belirleyiciler üç türde olabilir: **public**, **private** ve **protected**.

1. **public**:

- Public özellikler ve metotlar, sınıfın dışındaki her yerden erişilebilir.

- Varsayılan olarak, sınıf içinde tanımlanan her şey **public**’tir.

1. **private**:

- Private özellikler ve metotlar, yalnızca sınıfın içinde erişilebilir. Dışarıdan, hatta bu sınıftan türetilen alt sınıflardan bile erişilemez.

- Private özellikler, genellikle nesnenin iç durumunun korunmasını sağlamak için kullanılır.

1. **protected**:

- Protected özellikler ve metotlar, sadece sınıfın içinde ve o sınıfı miras alan alt sınıflarda erişilebilir.

- Bu, alt sınıfların üst sınıfın özelliklerine erişmesine izin verir, ancak dışarıdan erişim engellenir.

Yukarıdaki örnekte, **name** özelliği **protected** olarak tanımlanmıştır. Bu nedenle, **Dog** sınıfında this.name ifadesi geçerli olsa da, dışarıdan erişilemez.

### **Kodun Çalışma Prensibi**

- **Animal** sınıfı bir temel sınıf olarak name özelliğini tanımlar ve bu değeri getName metodu ile döndürür.

- **Dog** sınıfı ise Animal sınıfını genişleterek, name özelliğini ve ek olarak kendi family özelliğini ekler. getNamee metodunda, name özelliğine doğrudan erişim sağlanır.

```
const dog = new Dog("Labrador", "Canine");
dog.getNamee();  // Çıktı: undefined
```

Burada, dog.getNamee() metodunu çağırdığınızda **name** özelliği doğru şekilde görüntülenmez. Bunun nedeni, **getNamee** metodunun yalnızca name özelliğini konsola yazdırmaya çalışması ve doğru erişim metodunun **getName** olmasıdır.

### **Sonuç**

JavaScript’teki **sınıflar** nesne yönelimli programlamayı destekler ve kodunuzu daha düzenli ve tekrar kullanılabilir hale getirir. Kalıtım, alt sınıfların üst sınıflardan özellik ve metotları devralmasına olanak tanır. **public**, **private** ve **protected** erişim belirleyicileri, sınıf içindeki verilere erişimi yönetmek için kullanılır. Bu temel özellikler, daha esnek ve güvenli uygulamalar geliştirmek için önemlidir.

* * *

### **Abstract Classes**

**Abstract Classes (Soyut Sınıflar)**, nesne yönelimli programlamada, sınıflar arasında ortak bir şablon sağlamak için kullanılır. Soyut sınıflar, doğrudan nesne oluşturulamaz; bunun yerine, soyut sınıflardan türeyen alt sınıflar, soyut sınıfın sunduğu şablonları kullanarak işlevselliği tamamlar. Soyut sınıflar, genellikle bir sınıfın temel özelliklerini ve metotlarını tanımlar ve alt sınıfların bu özellikleri kendi gereksinimlerine göre şekillendirmesine olanak tanır.

Bir **abstract class** içinde tanımlanan **abstract method** (soyut metot), sadece metot adı ve alacağı parametreler gibi bir şablon içerir, fakat metotun içi soyut sınıf içinde tanımlanmaz. Bu metot, sadece alt sınıflar tarafından **implement** (uygulanmak) zorundadır.

### **Soyut Sınıf Tanımlaması**

Soyut bir sınıf, JavaScript’te **abstract** anahtar kelimesi ile tanımlanır. Bu sınıf, bazı metotları alt sınıflarına soyut olarak bırakırken, bazıları da tamamlanmış işlevselliğe sahip olabilir. Soyut sınıf içindeki soyut metotlar alt sınıflar tarafından uygulanmak zorundadır.

Örnek olarak bir **Car** sınıfı üzerinden soyut sınıf ve soyut metotların nasıl çalıştığını inceleyelim:

```
abstract class Car {
    brand: string;

    constructor(brand: string) {
        this.brand = brand;
    }

    abstract getBrand(duration: number): void;
}
```

Bu örnekte, **Car** sınıfı soyut olarak tanımlanmıştır. Bu sınıfın içinde **getBrand** adında soyut bir metot bulunmaktadır. Bu metot, sadece alacağı parametreyi (bu örnekte duration) tanımlar, ancak içinde yapılacak işlemler soyut sınıfta belirtilmez.

### **Soyut Sınıfın Kullanımı ve Alt Sınıflarda Implementasyon**

Bir soyut sınıf, **extends** anahtar kelimesi ile başka bir sınıf tarafından türetilebilir. Soyut sınıfı türeten alt sınıf, soyut metotları **implement** ederek işlevsellik kazandırmak zorundadır. Aşağıdaki örnekte, **SportCar** sınıfı **Car** sınıfından türemektedir ve **getBrand** metodunu uygulamaktadır.

```
class SportCar extends Car {
    getBrand(duration: number): void {
        console.log(this.brand);
    }
}
```

**SportCar** sınıfı, **Car** sınıfından türetilmiş bir alt sınıftır. **getBrand** metodu, soyut sınıf olan **Car** sınıfında yalnızca tanımlanan bir şablon olduğundan, **SportCar** sınıfında bu metot içeriğiyle tamamlanmıştır. Bu örnekte, getBrand metodu sadece **this.brand** bilgisini konsola yazdırmaktadır.

### **Soyut Sınıfın Avantajları**

1. **Ortak Şablon Sağlama**: Soyut sınıflar, birden fazla sınıfın ortak işlevselliğini belirler. Alt sınıflar, bu şablonu kendi ihtiyaçlarına göre tamamlar.

1. **Zorunlu Implementasyon**: Soyut metotlar, alt sınıflarda zorunlu olarak implement edilmelidir. Bu, programcıya bazı metotların her alt sınıfta uygulanması gerektiğini garanti eder.

1. **Genişletilebilirlik**: Soyut sınıflar, temel işlevselliği sağlar ve alt sınıfların üzerinde özel işlevler geliştirmelerine olanak tanır. Bu, kodun genişletilmesini ve bakımını kolaylaştırır.

### **Kodun Çalışma Prensibi**

1. **Car** sınıfı soyut olarak tanımlandığı için, doğrudan bir **Car** nesnesi oluşturulamaz.

1. **SportCar** sınıfı, **Car** sınıfından türemekte ve **getBrand** metodunu uygulamaktadır.

1. **getBrand** metodu, **SportCar** sınıfında ne yapılacağına karar veren bir metodudur ve **Car** sınıfında tanımlandığı şekilde yalnızca parametreyi alacak şekilde şablonlanmıştır.

**Çalıştırma Örneği**

```
const sportCar = new SportCar("Ferrari");
sportCar.getBrand(10);  // Çıktı: Ferrari
```

Burada, sportCar.getBrand(10) çağrısı **SportCar** sınıfındaki **getBrand** metodunu tetikler ve Ferrari markasını konsola yazdırır.

### **Sonuç**

Soyut sınıflar, nesne yönelimli programlamada güçlü bir yapıdır. Onlar, temel bir şablon oluşturur ve alt sınıfların bu şablon üzerinde özelleştirme yapmasına olanak tanır. Soyut metotlar, alt sınıfların kendi işlevselliklerini eklemelerini zorunlu kılarak, daha tutarlı ve hatasız bir yazılım geliştirilmesine yardımcı olur.

* * *

### **Classes and Interfaces**

**Classes** ve **Interfaces**, TypeScript’te nesne yönelimli programlamanın temel yapı taşlarıdır. Her ikisi de belirli bir yapıyı ve işlevselliği tanımlamak için kullanılır, ancak kullanım şekilleri ve amaçları farklıdır.

### **Interface Nedir?**

**Interface**, bir sınıfın sahip olması gereken **metodları** ve **özellikleri** tanımlar, ancak bu metodların ve özelliklerin içeriği hakkında herhangi bir bilgi vermez. Yani, bir interface yalnızca bir “şablon” sağlar ve bu şablonu uygulamak zorunda olan sınıflar, arayüzde belirtilen metotları kendi ihtiyaçlarına göre doldurur.

Interface’ler, bir sınıfın hangi metotları ve özellikleri içereceğini belirtmek için kullanılır, ancak bu metotların işlevselliğini tanımlamak sınıfın sorumluluğundadır.

### **Interface Kullanımı**

Bir sınıf, bir interface’i **implements** anahtar kelimesi ile uygulayabilir. Bu durumda sınıf, arayüzde belirtilen metotları uygulamak zorundadır.

Örnek olarak bir **Animal1** interface’i ve bu interface’i uygulayan bir **Bird** sınıfı üzerinden nasıl çalıştığını inceleyelim:

```
interface Animal1 {
    speak(): void;
}

class Bird implements Animal1 {
    speak(): void {
        console.log("Cik cik");
    }

    speak1(): void {
        console.log("Ciiiik ciiik");
    }
}
```

Bu örnekte:

1. **Animal1** adlı interface, **speak()** adında bir metodun varlığını belirtir. Ancak, metot ne yapacağına dair herhangi bir bilgi içermez. Bu metot, interface’i uygulayacak sınıf tarafından tanımlanmalıdır.

1. **Bird** sınıfı **Animal1** interface’ini **implements** anahtar kelimesiyle uygular. Bu sınıf, **Animal1** interface’indeki **speak()** metodunu tanımlar ve içeriğini belirler.

1. **Bird** sınıfı ayrıca **speak1()** adında bir başka metod tanımlar. Bu metod, sadece **Bird** sınıfına özgüdür ve **Animal1** interface’inde yer almaz.

### **Interface ile Nesne Oluşturma**

Interface üzerinden nesne oluşturulamaz; ancak bir sınıf bir interface’i uygularsa, o sınıfın nesneleri interface tipinde de tanımlanabilir. Örneğin, **bird1** değişkeni, **Animal1** interface’ini implement eden bir **Bird** sınıfına ait bir nesneyi tutmaktadır:

```
const bird1: Animal1 = new Bird();  // interface tipinde bir nesne
```

Bu örnekte, **bird1** değişkeni, **Animal1** interface’ine uygun bir **Bird** sınıfına ait nesne tutuyor. Bu durumda, yalnızca interface içinde tanımlanan metotlar erişilebilir. Yani **speak()** metodu kullanılabilir, ancak **speak1()** metodu kullanılamaz, çünkü bu metod sadece **Bird** sınıfına aittir.

Bir başka örnek:

```
const bird2: Bird = new Bird();  // Bird sınıfından doğrudan nesne
```

Burada, **bird2** değişkeni doğrudan **Bird** sınıfının nesnesi olarak tanımlanır. **Bird** sınıfındaki tüm metodlara erişim mümkündür, bu da **speak()** ve **speak1()** metotlarını içerir.

### **Public ve Private Erişim**

Bir interface içindeki metotlar **public** olarak tanımlanır, yani bu metotlar, interface’i implement eden sınıflar tarafından görünür ve erişilebilir olmalıdır. Eğer bir interface’deki metot **public** olarak tanımlandıysa, bu metot **private** veya **protected** olarak implement edilemez. Örneğin:

```
interface Animal1 {
    speak(): void;
}

class Bird implements Animal1 {
    // Error: Method 'speak' in class 'Bird' is private and cannot be accessed.
    private speak(): void {
        console.log("Cik cik");
    }
}
```

Yukarıdaki örnekte, **speak()** metodu **private** olarak tanımlandığında hata alırsınız. Çünkü **Animal1** interface’i içinde **speak()** metodu **public** olarak tanımlanmıştır ve sınıf içinde **private** tanımlanması mümkün değildir.

### **Kodun Çalışma Prensibi**

1. **Animal1** interface’i sadece **speak()** metodunun varlığını belirtir.

1. **Bird** sınıfı, **Animal1** interface’ini **implements** anahtar kelimesiyle uygular ve **speak()** metodunun içeriğini tanımlar.

1. **bird1** değişkeni, **Animal1** tipiyle tanımlanır, bu nedenle sadece interface’deki metotlara erişilebilir.

1. **bird2** değişkeni, **Bird** tipiyle tanımlandığı için sınıftaki tüm metotlara erişim mümkündür.

**Sonuç**

**Classes** ve **Interfaces**, TypeScript’te güçlü nesne yönelimli programlama özellikleridir. **Classes**, nesnelerin özelliklerini ve işlevselliğini tanımlarken, **Interfaces** sınıflara belirli bir yapıyı uygulama zorunluluğu getirir. Bu, kodun daha tutarlı ve yeniden kullanılabilir olmasını sağlar. Interface’ler, sınıfların implement ettiği metotları zorunlu kılarak, belirli bir yapının ve düzenin korunmasını sağlar.

* * *

## **Static Attributes and Methods**

**Static** nitelikler ve metotlar, nesne örneklerine (instances) değil, sınıfa (class) ait olan özelliklerdir. Yani, bir sınıfın statik özelliklerine veya metotlarına doğrudan sınıf üzerinden erişilebilir, sınıfın örnekleri üzerinden değil. Bu, belirli bir değerin tüm sınıf örneklerinde ortak olmasını sağlamak için kullanışlıdır.

### **Static Attributes (Statik Özellikler)**

Bir sınıfın **statik özellikleri**, sınıfın kendisine ait olup, bu özelliklere yalnızca sınıf ismi ile erişilebilir. Statik özellikler, sınıfın örnekleri (instances) oluşturulduğunda paylaşılmaz, yani her bir örnek ayrı bir kopya oluşturmaz. Bunun yerine, tüm sınıf örnekleri bu statik özellikleri **ortak** olarak paylaşır.

Örneğin, bir sınıfın kaç tane örneği oluşturulduğunu izlemek istiyorsanız, bu tür bir bilgiyi statik bir özellik olarak tanımlayabilirsiniz:

```
class Car1 {
    static instanceCount: number = 0;
    brand: string;

    constructor(brand: string) {
        this.brand = brand;
        Car1.instanceCount++; // her yeni örnek oluşturulduğunda instanceCount artırılır
    }

    static decreaseInstanceCount() {
        this.instanceCount--; // instanceCount statik metodu ile azaltılabilir
    }
}

const TofasSahin = new Car1("Tofas");

console.log(Car1.instanceCount); // 1, çünkü yalnızca bir örnek oluşturuldu
```

Yukarıdaki kodda:

- **instanceCount** statik bir özelliktir. Bu özellik, sınıfın kendisine aittir, örneklerine değil. Yani, **Car1.instanceCount** ile erişilir.

- **instanceCount** her yeni **Car1** örneği oluşturulduğunda artar. Bu, **constructor** içinde **Car1.instanceCount++** ifadesiyle yapılır.

- **decreaseInstanceCount()** ise **static** bir metottur ve bu metot sadece sınıf üzerinden çağrılabilir, nesne örneklerinden erişilemez.

### **Static Methods (Statik Metotlar)**

**Static metotlar**, sınıfın örneklerinden değil, sınıfın kendisinden çağrılabilen metodlardır. Bu metotlar da tıpkı statik özellikler gibi sadece sınıf düzeyinde çalışır, nesnelerle doğrudan ilişkili değildir.

Örneğin, sınıfın örnek sayısını güncellemek için kullanılan **decreaseInstanceCount()** metodu statik bir metottur. Bu metot, **Car1** sınıfı üzerinden çağrılabilir, ancak bir **Car1** örneğinden çağrılmaya çalışılamaz.

```
class Car1 {
    static instanceCount: number = 0;
    brand: string;

    constructor(brand: string) {
        this.brand = brand;
        Car1.instanceCount++;
    }

    static decreaseInstanceCount() {
        this.instanceCount--; // Sadece sınıf üzerinden erişilebilir
    }
}

const TofasSahin = new Car1("Tofas");
console.log(Car1.instanceCount); // 1

Car1.decreaseInstanceCount(); // Statik metot sınıf üzerinden çağrılabilir
console.log(Car1.instanceCount); // 0
```

Burada:

- **decreaseInstanceCount()** statik metodu, **Car1** sınıfının örneklerinden değil, doğrudan sınıf üzerinden çağrılmaktadır.

- **this.instanceCount** ifadesi ile **instanceCount** statik özelliği, sınıf üzerinden değiştirilir.

### **Statik Özelliklerin ve Metodların Kullanım Durumları**

Statik özellikler ve metotlar, genellikle şu durumlarda kullanılır:

1. **Ortak Veriler**: Bütün sınıf örneklerinin aynı veriyi paylaşmasını sağlamak için.

1. **Nesne Sayısını İzleme**: Örneğin, bir sınıfın kaç örneği oluşturulduğunu saymak gibi durumlar.

1. **Yardımcı Fonksiyonlar**: Nesne örneklerinden bağımsız çalışan yardımcı fonksiyonlar için.

### **Kodda Statik Özelliklere ve Metotlara Erişim**

Statik özellikler ve metotlar, her zaman **sınıf adı** üzerinden erişilir. Örneğin, **Car1.instanceCount** ve **Car1.decreaseInstanceCount()** gibi.

```
console.log(Car1.instanceCount); // instanceCount'a sınıf adı üzerinden erişilir
Car1.decreaseInstanceCount(); // decreaseInstanceCount metodu da sınıf adı üzerinden çağrılır
```

Bir nesne örneğinden statik özelliklere veya metotlara erişmeye çalışmak hata verecektir:

```
const car = new Car1("Tofas");
console.log(car.instanceCount); // Error! instanceCount statik bir özelliktir ve sınıfın kendisine aittir, nesneye ait değildir.
car.decreaseInstanceCount(); // Error! decreaseInstanceCount, statik bir metottur ve nesne üzerinden çağrılamaz.
```

### **Sonuç**

**Static** özellikler ve metotlar, sınıf düzeyinde paylaşılan verilere ve fonksiyonlara erişimi sağlar. Bunlar, sınıfın tüm örnekleri arasında ortak bir durumu yönetmek için kullanılır. Statik metotlar, nesne örneklerinden bağımsız çalışır ve sadece sınıf adı üzerinden çağrılabilir.

* * *

## **Generics**

**Generics**, TypeScript’in güçlü tip sistemi özelliklerinden biridir. Genellikle bir sınıf, fonksiyon veya arayüz (interface) ile çalışma sırasında veri türünü **dinamik** olarak belirlemeyi sağlar. Bu sayede kodun daha esnek, yeniden kullanılabilir ve tip güvenli hale gelmesini sağlar.

Genel olarak, **generics** veri türlerini **parametre olarak alabilen** yapılar olarak tanımlanabilir. Bu tür yapılarla, belirli bir fonksiyon veya sınıf her türden veri tipi ile çalışabilir, ancak yine de belirli bir veri tipi üzerinde işlem yapmaya devam eder.

### **Generics ile Fonksiyonlar**

Generics kullanarak, fonksiyonların kabul ettiği veri tipini belirleyebiliriz. Bu, özellikle aynı fonksiyonu farklı veri tipleriyle kullanmamız gerektiğinde faydalıdır. Aşağıda, generics kullanılarak yazılmış bir fonksiyon örneği yer almaktadır:

```
function identity<T>(arg: T): T {
    return arg;
}

console.log(identity(42));      // 42
console.log(identity("Hello")); // "Hello"
```

Burada:

- **<T>** bir **generic parametre**dir. Bu, fonksiyonun aldığı argümanın türünün belirlenmesini sağlar.

- identity fonksiyonu, hangi türde bir argüman alırsa, o türde bir değer döndürür. Bu durumda, T yerini fonksiyon çağırıldığı anda geçer.

**identity(42)** çağrısında T, number olarak belirlenir, ve **identity("Hello")** çağrısında T, string olarak belirlenir. Bu sayede aynı fonksiyon, farklı veri türleriyle çalışabilir.

### **Generics ile Sınıflar**

**Generics**, sınıflarla birlikte de kullanılabilir. Bu, belirli bir türle çalışan sınıflar oluştururken daha fazla esneklik sağlar.

```
class Box<T> {
    content: T;

    constructor(content: T) {
        this.content = content;
    }

    getContent(): T {
        return this.content;
    }
}

const numberBox = new Box(123);
console.log(numberBox.getContent()); // 123

const stringBox = new Box("Hello");
console.log(stringBox.getContent()); // "Hello"
```

Burada:

- **Box<T>** sınıfı, bir **generic sınıf**tır. Bu sınıfın content özelliği, parametre olarak alınan **T** türüne göre belirlenir.

- **Box(123)** çağrısında, T türü **number** olarak belirlenir.

- **Box("Hello")** çağrısında ise, T türü **string** olarak belirlenir.

### **Generics ile Arayüzler (Interfaces)**

Generics, arayüzlerle de kullanılabilir. Bu, tür güvenliği sağlarken daha esnek arayüzler oluşturulmasına olanak tanır.

```
interface Pair<T, U> {
    first: T;
    second: U;
}

const pair: Pair<number, string> = { first: 1, second: "apple" };
console.log(pair.first);   // 1
console.log(pair.second);  // "apple"
```

Burada:

- **Pair<T, U>** arayüzü, iki parametreli bir generic arayüzdür. T ve U, iki farklı türü temsil eder.

- pair değişkeni, number ve string türlerinde iki değer alır.

### **Kısıtlamalar ile Generics (Constraints)**

**Generics** kullanırken, belirli bir tür kısıtlaması (constraint) eklemek mümkündür. Bu, sadece belirli bir türü kabul eden generic yapılar oluşturmanıza olanak sağlar.

Örneğin, aşağıdaki örnekte **T** türünün yalnızca string veya number türleriyle sınırlı olması sağlanmaktadır:

```
function logLength<T extends string | number>(value: T): void {
    console.log(value.length);  // length özelliği yalnızca string ve number türlerinde vardır
}

logLength("Hello"); // "Hello".length = 5
logLength(12345);   // 12345.length = 5

logLength(true);    // Error: Argument of type 'boolean' is not assignable to parameter of type 'string | number'.
```

Burada:

- **T extends string | number** ifadesi, **T** türünün **string** veya **number** türlerinden biri olabileceğini belirtir. Bu sayede logLength fonksiyonu yalnızca bu türleri kabul eder.

- **value.length** özelliği yalnızca string ve number türlerinde mevcut olduğu için, **logLength(true)** çağrısı hata verir.

### **Generics ile Diziler**

**Generics** ayrıca dizilerle de kullanılarak daha tür güvenli diziler oluşturulmasını sağlar.

```
function wrapInArray<T>(value: T): T[] {
    return [value];
}

const numberArray = wrapInArray(42);    // number[] 
const stringArray = wrapInArray("Hello"); // string[] 

console.log(numberArray); // [42]
console.log(stringArray); // ["Hello"]
```

Burada, **wrapInArray** fonksiyonu, tür güvenli bir şekilde değerleri diziye sarar. **T\[\]** ifadesi, fonksiyonun döndüreceği değerin bir dizi olduğunu belirtir ve bu dizinin türü T olur.

### **Sonuç**

**Generics**, TypeScript’te esnek, tekrar kullanılabilir ve tip güvenli kodlar yazmak için güçlü bir araçtır. Sınıflar, fonksiyonlar ve arayüzlerle birlikte kullanılarak kodunuzu daha modüler, okunabilir ve hatalardan arındırılmış hale getirir. Generics ile türleri parametre olarak alabilir, kısıtlamalar ekleyebilir ve farklı veri tipleriyle çalışabilirken her zaman tür güvenliğini koruyabilirsiniz.

* * *

## **Type Aliases**

**Type aliases**, TypeScript’te yeni veri türlerini tanımlamak için kullanılan bir özelliktir. Bir tür alias’ı (takma adı), daha önce tanımlı olan bir türü bir adla ilişkilendirerek, o türü kullanacağınız her yerde bu alias’ı kullanmanıza olanak tanır. Bu, kodunuzu daha okunabilir ve yönetilebilir hale getirir.

### **Type Alias Nedir?**

Bir **type alias** (tip takma adı), genellikle type anahtar kelimesiyle tanımlanır ve belirli bir türü daha anlamlı bir isimle ilişkilendirir. Type aliases, nesneler, fonksiyonlar, diziler gibi birçok türü tanımlamak için kullanılabilir.

### **Basit Bir Type Alias Kullanımı**

Aşağıda, basit bir **type alias** örneği yer almaktadır:

```
type Name = string;

let firstName: Name = "John";
let lastName: Name = "Doe";
```

Burada:

- **type Name = string;** ifadesi, Name adında bir alias tanımlar ve bu alias, string türüyle eşdeğerdir.

- Daha sonra **firstName** ve **lastName** değişkenleri **Name** türünde tanımlanmıştır.

### **Nesneler İçin Type Aliases**

Type aliases, nesneleri tanımlamak için de yaygın olarak kullanılır. Bu sayede nesnelerin yapılarını daha kolay bir şekilde belirleyebiliriz.

```
type Person = {
    name: string;
    age: number;
    address: string;
};

let user: Person = {
    name: "Alice",
    age: 30,
    address: "123 Main St"
};
```

Burada:

- **type Person = { ... }** ifadesi, **Person** adında bir alias oluşturur ve bu alias bir nesne tipini temsil eder. Bu nesne, **name**, **age**, ve **address** gibi özelliklere sahip olmalıdır.

- **user** değişkeni, Person alias’ına uygun bir nesne olarak tanımlanmıştır.

### **Fonksiyonlar İçin Type Aliases**

Type aliases, fonksiyon türlerini tanımlamak için de kullanılabilir. Bu, bir fonksiyonun aldığı parametrelerin ve döndürdüğü değerin türünü belirlemek için faydalıdır.

```
type GreetFunction = (name: string) => string;

const greet: GreetFunction = (name) => {
    return `Hello, ${name}`;
};

console.log(greet("World")); // "Hello, World"
```

Burada:

- **type GreetFunction = (name: string) => string;** ifadesi, bir fonksiyon türü tanımlar. Bu fonksiyon bir string parametre alır ve string türünde bir değer döndürür.

- **greet** fonksiyonu, **GreetFunction** alias’ına uygun şekilde tanımlanmıştır.

### **Union Types (Birleşim Türleri) ve Type Aliases**

Type aliases, **union types** (birleşim türleri) ile de kullanılabilir. Birleşim türü, bir değerin birden fazla türden biri olabileceğini belirtir.

```
type StringOrNumber = string | number;

let value1: StringOrNumber = "Hello";
let value2: StringOrNumber = 42;
```

Burada:

- **type StringOrNumber = string | number;** ifadesi, StringOrNumber adında bir alias tanımlar. Bu alias, ya **string** ya da **number** türünden bir değeri kabul eder.

- **value1** ve **value2** değişkenleri, **StringOrNumber** türünde tanımlanmıştır ve her ikisi de geçerli türlerdir.

### **Intersection Types (Kesişim Türleri) ve Type Aliases**

Type aliases, **intersection types** (kesişim türleri) ile de kullanılabilir. Kesişim türü, bir değerin birden fazla türü aynı anda taşıması gerektiğini belirtir.

```
type Employee = {
    id: number;
    name: string;
};

type Manager = Employee & {
    department: string;
};

const manager: Manager = {
    id: 1,
    name: "John Doe",
    department: "HR"
};
```

Burada:

- **type Manager = Employee & { ... };** ifadesi, Manager alias’ını tanımlar. Bu alias, Employee türünü ve ek olarak **department** özelliğini içeren bir türdür.

- **manager** değişkeni, her iki türü de taşıyan bir nesne olarak tanımlanmıştır.

### **Type Aliases ve Tuple’lar**

Type aliases, **tuple** (değer dizisi) türlerini tanımlamak için de kullanılabilir. Tuple, sabit sayıda ve sabit türlerdeki öğeleri içeren bir dizidir.

```
type Point = [number, number];

let point: Point = [10, 20];
```

Burada:

- **type Point = \[number, number\];** ifadesi, **Point** alias’ını bir tuple olarak tanımlar. Bu tuple, iki adet **number** türünde öğe içerir.

- **point** değişkeni, Point alias’ına uygun şekilde bir tuple olarak tanımlanmıştır.

### **Tip Aliases ile Daha Karmaşık Yapılar**

Birden fazla birleşim ve kesişim türüyle daha karmaşık yapılar oluşturmak mümkündür. Bu tür yapılar, daha büyük ve daha esnek projelerde faydalı olabilir.

```
type ContactInfo = {
    email: string;
    phone: string;
};

type User = {
    name: string;
    contact: ContactInfo;
} & {
    age: number;
};

let user: User = {
    name: "Jane",
    contact: {
        email: "jane@example.com",
        phone: "123-456-7890"
    },
    age: 25
};
```

Burada:

- **ContactInfo** ve **User** tipleri birleştirilerek karmaşık bir yapı oluşturulmuştur.

- **user** değişkeni, hem **name** ve **contact** özelliklerini hem de **age** özelliğini içeren bir nesne olarak tanımlanmıştır.

### **Sonuç**

**Type aliases**, TypeScript’te kodunuzu daha esnek, okunabilir ve sürdürülebilir hale getiren güçlü bir araçtır. Farklı türleri tanımlamak için kullanabilir, fonksiyon türlerini belirleyebilir, birleşim ve kesişim türlerini kolayca tanımlayabilirsiniz. Bu sayede kodunuzu daha modüler hale getirebilir ve tür güvenliğini artırabilirsiniz.

* * *

## **Union ve Intersection Types**

TypeScript’te **Union Types** (Birleşim Türleri) ve **Intersection Types** (Kesişim Türleri) türler, çok daha esnek ve güçlü tip kontrolü sağlar. Bu iki tür, veri yapılarınızda çoklu türlerin bir arada kullanılmasını sağlayarak daha esnek bir programlama deneyimi sunar.

### **Union Types (Birleşim Türleri)**

**Union types**, bir değerin birden fazla türden birini kabul etmesini sağlar. Yani, bir değişkenin değeri birden fazla farklı türde olabilir. Birleşim türü, | (pipe) operatörü ile tanımlanır.

**Union Types Örneği:**

```
interface Interface1 {
    a: number;
}

interface Interface12 {
    b: string;
}

type X = Interface1 | Interface12; // İki interfaceden bir tanesi olabilir
```

Bu örnekte, **X** türü bir **Interface1** ya da **Interface12** türünden bir nesne olabilir. Bu durumda, **X** türündeki bir değişken yalnızca bu iki interface’ten birine ait özellikleri içerebilir.

- Eğer bir **X** türünde bir değişken **Interface1** türündeyse, **a** özelliği bulunur.

- Eğer bir **X** türünde bir değişken **Interface12** türündeyse, **b** özelliği bulunur.

```
const obj1: X = { a: 5 }; // Geçerli, çünkü Interface1 türü
const obj2: X = { b: "Hello" }; // Geçerli, çünkü Interface12 türü
const obj3: X = { a: 5, b: "Hello" }; // Geçerli, çünkü objeler Interface1 veya Interface12 olabilir
```

Bu durumda, obj1 yalnızca **a** özelliğini içerebilirken, obj2 yalnızca **b** özelliğini içerebilir. obj3 hem **a** hem de **b** özelliğine sahip olsa da, **X** türünde geçerlidir çünkü bir nesne yalnızca bir birleşim türü olarak kabul edilir.

### **Union Types’ın Kullanım Alanları:**

Union types, bir değişkenin değeri, belirli türlerden birini kabul edebiliyorsa kullanılır. Örneğin, bir fonksiyon hem string hem de number türündeki parametreleri kabul edebilir.

```
type StringOrNumber = string | number;

function printValue(value: StringOrNumber) {
    console.log(value);
}

printValue("Hello"); // Geçerli
printValue(123); // Geçerli
```

### **Intersection Types (Kesişim Türleri)**

**Intersection types**, bir değerin iki ya da daha fazla türü aynı anda taşımasını sağlar. Kesişim türü, & (and) operatörü ile tanımlanır. Bu durumda, bir değişken hem bir türün hem de diğer türlerin tüm özelliklerine sahip olmalıdır.

**Intersection Types Örneği:**

```
type Y = Interface1 & Interface12; // İki interface'in de bütün değerlerine sahip olmalıdır.
```

Bu örnekte, **Y** türü, hem **Interface1** hem de **Interface12** türlerinin tüm özelliklerine sahip olmalıdır. Yani, **Y** türünde bir nesne her iki interface’in tüm özelliklerine sahip olmalıdır.

```
const obj: Y = {
    a: 5,  // Interface1'den
    b: "Hello" // Interface12'den
};
```

Burada, **obj** değişkeni **Interface1** türündeki **a** özelliği ve **Interface12** türündeki **b** özelliğini içermek zorundadır. Yani her iki interface’in de tüm özellikleri **obj** nesnesinde yer almalıdır.

### **Intersection Types’ın Kullanım Alanları:**

Intersection types, bir nesnenin birden fazla türün tüm özelliklerine sahip olması gerektiğinde kullanılır. Örneğin, bir nesne birden fazla özellik grubu taşıyorsa, her iki grubun özelliklerine erişmek için kesişim türü kullanılabilir.

```
type Employee = {
    id: number;
    name: string;
};

type Manager = Employee & {
    department: string;
};

const manager: Manager = {
    id: 1,
    name: "Alice",
    department: "HR"
};
```

Burada, **Manager** türü, hem **Employee** türündeki **id** ve **name** özelliklerine hem de **department** özelliğine sahip olmalıdır.

### **Union ve Intersection Türlerinin Farkları**

1. **Union Types (|)**: Bir değer, belirtilen türlerden herhangi birine sahip olabilir. Yani, bir değişken birden fazla türden birini kabul eder.

- Örneğin, string | number türü, ya string ya da number olabilir.

1. **Intersection Types (&)**: Bir değer, belirtilen tüm türlere sahip olmalıdır. Yani, bir değişken birden fazla türün tüm özelliklerini taşımalıdır.

- Örneğin, Employee & Manager türü, hem Employee hem de Manager türlerinin tüm özelliklerine sahip olmalıdır.

### **Sonuç**

Union ve Intersection Types, TypeScript’te çok güçlü araçlardır. **Union types**, bir değerin birden fazla türden birine sahip olmasına izin verirken, **Intersection types**, bir değerin birden fazla türün tüm özelliklerine sahip olmasını sağlar. Bu özellikler, özellikle daha büyük ve karmaşık projelerde esnekliği ve tip güvenliğini artırarak hata oranını azaltır.

* * *

## **Type Aliases**

**Type aliases** (tip takma adları), TypeScript’te var olan türleri yeniden adlandırarak onları daha kolay ve anlamlı bir şekilde kullanmamızı sağlar. Type aliases, kodu daha temiz ve okunabilir hale getirmek için oldukça kullanışlıdır. Ancak, **type aliases** ile **interfaces** arasında bazı önemli farklar vardır. Özellikle, **type aliases**’lar extends ve implements gibi özelliklere sahip olamazken, **interfaces** bunları destekler.

### **Type Aliases Kullanımı**

Type aliases, genellikle karmaşık türleri daha anlaşılır ve kısa hale getirmek amacıyla kullanılır. Bir **type alias**, temel olarak bir tür tanımlaması sağlar ve bu tanım, belirtilen türün bir takma adı olur. Type alias’lar, her türlü türü, yani basit türlerden (örneğin string, number), daha karmaşık türlerden (örneğin, tuple, array veya union) türetilmiş türleri alabilir.

**Örnek - Type Alias ile Tuple Tanımlama:**

```
type Coordinate = [number, number];

function compareCords2(x: Coordinate, y: Coordinate): Coordinate {
    return [x[0], y[1]];
}
```

Bu örnekte, Coordinate adı verilen bir **type alias** oluşturulmuş ve bu alias, bir **tuple**‘ı (iki adet number içeren bir liste) temsil ediyor. Fonksiyonlarda, tiplerin yeniden kullanılabilirliğini artırmak için Coordinate alias’ı kullanılmıştır.

**Avantajları:**

- **Daha Temiz Kod:** Aynı türü birden fazla yerde kullanmak yerine, her seferinde yazmak yerine bir alias (takma ad) kullanarak kodu daha kısa ve okunabilir hale getirirsiniz.

- **Esneklik:** Karmaşık türleri tanımlamak için oldukça kullanışlıdır, özellikle tuplar veya birleşim türleri gibi veri yapılarında.

### **Type Alias ve Fonksiyonlar**

Type alias’lar, fonksiyon parametrelerinin ve dönüş değerlerinin tiplerini belirtmek için de kullanılabilir. Fonksiyonlarda aynı türü tekrar tekrar yazmak yerine, bir alias ile kodunuzu daha temiz ve anlaşılır hale getirebilirsiniz.

```
function compareCords(x: [number, number], y: [number, number]): [number, number] {
    return [x[0], y[1]];
}
```

Bu fonksiyon compareCords, iki **tuple** parametresi alır ve bir **tuple** döndürür. Ancak, daha önce gördüğümüz gibi, bu tür bir fonksiyonu **type alias** kullanarak daha kısa ve anlaşılır hale getirebiliriz.

### **Type Aliases ile Daha Temiz Kod:**

```
type Coordinate = [number, number];

function compareCords2(x: Coordinate, y: Coordinate): Coordinate {
    return [x[0], y[1]];
}
```

Bu şekilde, her seferinde \[number, number\] yazmak yerine Coordinate alias’ını kullanarak kodu daha temiz ve yönetilebilir hale getiriyoruz.

### **Type Aliases ile Interface Farkları**

Type alias’lar ve **interface**’ler arasında bazı temel farklar vardır:

1. **Extend ve Implement:** Type alias’lar, **extends** ve **implements** gibi özelliklere sahip değildir. Yani bir **type alias** bir başka türü genişletemez veya bir sınıf tarafından implement edilemez. Bu özellikler yalnızca **interface**’ler için geçerlidir.

- Type alias’lar yalnızca tür tanımlamak için kullanılır.

- Interface’ler ise daha çok nesne ve sınıf yapılarında kullanılır ve genişletilebilir.

1. **Esneklik:** Type alias’lar daha esnektir ve türlerin birleşimlerini, kesişimlerini, union türlerini gibi daha karmaşık yapıları temsil etmek için kullanılabilir. Interface’ler ise daha çok nesnelerle ve sınıflarla sınırlıdır.

## **Interface ve Type Alias Karşılaştırması:**

```
interface Point {
    x: number;
    y: number;
}

type Coordinate = [number, number];
```

- **Interface**: **Point** nesne türünde bir yapı oluşturur. x ve y özelliklerine sahip olmalıdır.

- **Type Alias**: **Coordinate** tuple türünde bir yapı oluşturur. Bu türde iki sayı bulunmalıdır.

## **Sonuç**

- **Type aliases**’lar, özellikle tekrar eden türleri tanımlamak ve daha temiz, daha yönetilebilir kod yazmak için kullanılır. Bu türler genellikle birleşim (union) veya kesişim (intersection) türleri gibi karmaşık türleri temsil etmek için idealdir.

- **Interfaces**, nesnelerin yapısal türlerini tanımlamak için kullanılır ve sınıflar veya nesneler arasında daha güçlü tip kontrolü sağlamak için uygundur. Ayrıca, **extends** ve **implements** gibi özelliklerle genişletilebilir.

Type alias’lar genellikle daha basit ve anlaşılır tür tanımlamaları sağlarken, interfaces daha karmaşık ve sınıf tabanlı yapılar için uygundur.

* * *

## **Type Guards (typeof, instanceof, is, in)**

**Type guards** (tip korumaları), TypeScript’te bir değerin belirli bir türde olup olmadığını kontrol etmemizi sağlayan yapılardır. Bu korumalar, kodun tür güvenliğini artırmaya yardımcı olur ve hata olasılığını azaltır. TypeScript, tiplerin doğru kullanıldığını denetlerken bazı durumlarda bu denetimleri manuel olarak yapmamıza olanak tanır. Bu tür korumalar sayesinde, belirli bir türle çalışırken doğru türdeki verilerle işlem yapabiliriz.

Aşağıda, TypeScript’te yaygın olarak kullanılan **type guards** türleri ve bunların nasıl kullanıldığını detaylı bir şekilde inceleyeceğiz.

## **typeof Type Guard**

**typeof** operatörü, bir değerin türünü kontrol etmek için kullanılır. Ancak, typeof yalnızca temel türler için işe yarar. Yani, sayılar, dizeler, boolean değerleri gibi ilkel türler üzerinde geçerlidir.

**Örnek: typeof ile Type Guard Kullanımı**

```
function getLength(input: string | number): number {
    if (typeof input === 'string') {
        return input.length; // input bir string ise, length özelliğini kullanabiliriz.
    } else {
        return input.toString().length; // input bir number ise, önce string'e çevirip length hesaplanabilir.
    }
}
```

Bu örnekte, input parametresi hem string hem de number olabilir. typeof operatörü kullanarak input‘un türünü kontrol ediyoruz. Eğer input bir string ise, length özelliği kullanılabilir. Eğer input bir number ise, önce toString() metodu ile string’e çevrilip ardından length alınır.

## **instanceof Type Guard**

**instanceof** operatörü, bir nesnenin belirli bir sınıfın örneği olup olmadığını kontrol eder. Bu, özellikle nesne tabanlı türlerde (sınıflarda) kullanılır. instanceof, yalnızca nesneler için geçerli olup, sınıfın türünü belirler.

**Örnek: instanceof ile Type Guard Kullanımı**

```
class Dog {
    bark() {
        console.log('Woof!');
    }
}

class Cat {
    meow() {
        console.log('Meow!');
    }
}

function makeSound(animal: Dog | Cat) {
    if (animal instanceof Dog) {
        animal.bark(); // animal Dog türünde ise, bark metodunu çağırabiliriz.
    } else {
        animal.meow(); // animal Cat türünde ise, meow metodunu çağırabiliriz.
    }
}
```

Bu örnekte, animal parametresi hem Dog hem de Cat türünde olabilir. instanceof operatörü kullanarak, hangi sınıfın örneği olduğunu kontrol ediyoruz ve uygun metodu çağırıyoruz.

## **in Type Guard**

**in** operatörü, bir nesnede belirli bir özelliğin olup olmadığını kontrol etmek için kullanılır. Bu, nesne tabanlı türlerde bir özellik veya metodu kontrol etmek için idealdir.

**Örnek: in ile Type Guard Kullanımı**

```
interface Dog {
    bark(): void;
}

interface Cat {
    meow(): void;
}

function makeSound(animal: Dog | Cat) {
    if ('bark' in animal) {
        animal.bark(); // Eğer 'bark' özelliği varsa, Dog türünde olduğunu varsayabiliriz.
    } else {
        animal.meow(); // Eğer 'bark' yoksa, Cat türünde olduğunu varsayabiliriz.
    }
}
```

Bu örnekte, animal nesnesinin bark özelliğine sahip olup olmadığını kontrol ediyoruz. Eğer bark özelliği varsa, bu nesnenin Dog türünde olduğunu kabul edebiliriz, aksi takdirde Cat türünde olduğunu varsayabiliriz.

### **Kullanıcı Tanımlı Type Guards (Custom Type Guards)**

TypeScript’te kullanıcı tanımlı type guard’lar da oluşturulabilir. Bu, bir fonksiyonun belirli bir türü tanıyıp ona göre farklı işlemler yapmasını sağlar. Kullanıcı tanımlı type guard’lar, **is** anahtar kelimesi ile tanımlanır.

**Örnek: Kullanıcı Tanımlı Type Guard Kullanımı**

```
interface Dog {
    bark(): void;
}

interface Cat {
    meow(): void;
}

function isDog(animal: Dog | Cat): animal is Dog {
    return (animal as Dog).bark !== undefined;
}

function makeSound(animal: Dog | Cat) {
    if (isDog(animal)) {
        animal.bark(); // Eğer isDog fonksiyonu true dönerse, animal bir Dog'dur.
    } else {
        animal.meow(); // Eğer false dönerse, animal bir Cat'tir.
    }
}
```

Bu örnekte, **isDog** fonksiyonu, bir Dog türü olup olmadığını kontrol eden kullanıcı tanımlı bir type guard’tır. isDog fonksiyonu, **animal is Dog** döndüren bir tür koruyucu fonksiyondur. Bu sayede makeSound fonksiyonu içinde animal’ın türünü güvenle kontrol edebiliriz.

**Sonuç**

TypeScript’te kullanılan **type guards**, tür güvenliğini artırarak kodun daha güvenilir hale gelmesini sağlar. Bu korumalar, tip hatalarını önlemek ve doğru türlerle çalışmak için güçlü araçlardır. **typeof**, **instanceof**, **in** ve **is** gibi yapılar, tip kontrolü yapmak için en yaygın kullanılan yöntemlerdir. Bu türler sayesinde, belirli bir değerin türünü kontrol edebilir ve ona göre işlemler gerçekleştirebiliriz.

* * *

## **Namespaces**

**Namespaces** (ad alanları), TypeScript’te bir grup ilgili kodu bir arada tutmak için kullanılan bir yapıdır. Temelde, bir projede birden fazla isimli öğe (fonksiyonlar, sınıflar, değişkenler, vs.) arasında ad çakışmalarını önlemek amacıyla kullanılır. Namespace’ler, genellikle eski projelerde ya da JavaScript’in modüler yapısının daha az kullanıldığı zamanlarda tercih edilmiştir. Ancak günümüzde, **ES6 modülleri** (import/export) daha yaygın olarak tercih edilmektedir.

### **Namespace Kullanımı**

Namespace kullanımı, ad çakışmalarını engellemek ve kodu daha düzenli tutmak için faydalıdır. Bir namespace içerisinde, başka fonksiyonlar, sınıflar ve değişkenler tanımlanabilir. Ancak, **ES6 modülleri** ile karşılaştırıldığında, namespace’ler daha az esneklik ve daha karmaşık bir yapıya sahiptir.

**Örnek: Namespace Tanımlama ve Kullanma**

```
namespace Animal {
    export class Dog {
        bark() {
            console.log("Woof!");
        }
    }

    export class Cat {
        meow() {
            console.log("Meow!");
        }
    }
}

const dog = new Animal.Dog();
dog.bark(); // Woof!

const cat = new Animal.Cat();
cat.meow(); // Meow!
```

Yukarıdaki örnekte, Animal adında bir namespace tanımladık. İçerisinde Dog ve Cat adında iki sınıf var. Her iki sınıf da export anahtar kelimesi ile dışarıya açılmıştır. Bu sayede Animal.Dog ve Animal.Cat şeklinde bu sınıflara erişilebilir.

### **Namespace İçi Fonksiyonlar ve Değişkenler**

Namespace’ler, sadece sınıfları değil, fonksiyonları ve değişkenleri de kapsayabilir. Böylece, ilgili tüm kodu tek bir alan altında gruplayabilirsiniz.

```
namespace MathUtils {
    export function add(x: number, y: number): number {
        return x + y;
    }

    export function multiply(x: number, y: number): number {
        return x * y;
    }
}

console.log(MathUtils.add(2, 3)); // 5
console.log(MathUtils.multiply(2, 3)); // 6
```

Bu örnekte, MathUtils namespace’inin içinde iki fonksiyon tanımlanmıştır: add ve multiply. Bu fonksiyonlar dışarıya açılmıştır, bu sayede MathUtils.add() ve MathUtils.multiply() şeklinde fonksiyonlara erişilebilir.

### **Namespace ve Modüller Arasındaki Farklar**

- **Namespace**: Daha eski bir yapıdır ve genellikle global scope üzerinde çalışır. Bir namespace, tek bir dosya içinde tanımlanabilir veya farklı dosyalara yayılabilir. Ancak bu, genellikle karmaşıklığa yol açabilir.

- **Modüller (ES6)**: Modern JavaScript kodlamasında, import ve export kullanılarak modüler yapılar oluşturulabilir. Modüller, her dosyada kendi scope’u ile çalışır ve daha esnektir.

### **Namespace Kullanımının Dezavantajları**

- **Global Scope Kirlenmesi**: Namespace kullanımı global scope üzerinde çalıştığı için, büyük projelerde kod karmaşası ve çakışmalar oluşabilir.

- **ES6 Modüllerinin Yerine Geçememesi**: ES6 modülleri, namespace’lere göre daha güçlü ve esnek bir yapıya sahiptir. Modüller, her dosyanın kendi bağımsız scope’u içinde çalışmasına olanak tanır.

### **Tavsiye Edilmeyen Kullanım**

Namespace’ler, modern TypeScript projelerinde çok yaygın kullanılmaz çünkü modüler yapılar (import/export) çok daha temiz ve esnektir. Ancak, eski projelerde veya belirli durumlarda namespace kullanımı gerekebilir. Bu yüzden, eski projelerde namespace’lerin nasıl çalıştığını bilmek faydalıdır, ancak yeni projelerde genellikle **ES6 modülleri** tercih edilmelidir.

### **Sonuç**

Namespace’ler, kodun düzenli ve çakışmasız bir şekilde organize edilmesine yardımcı olsa da, modern TypeScript projelerinde genellikle **ES6 modülleri** tercih edilmektedir. Çünkü modüller, her dosyanın kendi bağımsız scope’u ile çalışmasına olanak tanır ve daha güçlü, esnek bir yapıya sahiptir. Bu nedenle, namespace’ler yalnızca eski projelerde veya belirli kullanım senaryolarında faydalı olabilir.