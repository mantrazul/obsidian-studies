
### What is Character Encoding in HTML

Character encoding is basically a **mapping technique to define text and bytes** separately within HTML documents. To understand character encoding, authors must understand what characters are.

#### What are Characters in Coding Languages

**Characters denote** alphabetic letters, punctuation, special characters, and some other elements that make up the entire content. The information is stored in a computer as a sequence of bytes in numeric values. A single character can sometimes be represented by more than one byte.

Text, images, graphics, video, data compilations, and all other forms of information that appear to the website reader are **made up of "characters"** in a web page content.

> [!NOTE]
> What key was used to encode the text determines how the sequence of bytes is converted to characters. In this case, the key is referred to as character encoding.

#### The Importance of URLs
A [URL](How%20Does%20the%20Web%20Work.md) is used by web browsers to request pages from web servers. Web browsers can only decipher the ASCII character set, which only has 128 characters, and only 95 out of which are printable.

But URL often need characters outside of the 128 characters. **Character encoding is used to define the foreign character** sets in this case.

On the browser side, **documents wtih different HTML encodings would appear differently**. It is in the control and disposal of the markup author to use them appropriately.

### Understanding the ASCII Charset in the HTML Character Encoding Reference.

#### ASCII

**ASCII** is a **transmission code** derived from the American Standard Code for Information interchange that was created in the 1960s. It would be used on basic eletronic devices and computers to exchange letters, punctuation and numbers and **control characters that are non-printable** characters based on telex technology such as line-breaks or taps.

The ASCII codes work a lot like how calculators work wherein binary systems run the entire computational system. **Within seven bits** – seven digits that indicate either a zero or a one – the **original ASCII standard defines different characters**. It altogether defines only 128 (27) characters, out of which there are 33 non-printable and 95 printable characters.

Traditionally, the eighth bit, which is one full byte, is **still used to check data**. This exact bit is used in the ASCII-based extended versions to increase the number of available characters to 256. (28).

Even though the **UTF-8 charset** has become **more important when presenting text**, the 7-bit ASCII version is still widely used today. UTF-8 has the privilege of being quite backward-compatible since **it is a subset of ASCII.** Therefore,  it recognizes the binary 128 characters. The old encoding method is still used in emails and URLs because ASCII is the lowest common denominator of most new encoding forms.

### HTML Encoding UTF 8 Character Set

There are **several benefits to using UTF-8**, but above all, it is fully compatible with the ASCII special characters, which makes it the go-to tool for writing markup for foreign language pages.

Furthermore, it can be used with native XML markup also. **To declare UTF-8 encoded HTML character sets**, you need the following tag:

```html
<meta charset=”UTF-8″>
```

Insert a meta tag followed by a charset attribute, and **set UTF-8 as the character value**.

**Many languages can be supported by Unicode-based encodings like UTF-8**, which can accommodate pages and forms in any combination of those languages. So your content is free from the rule of server-side logic to display the character encoding for each page served for individual form submissions.

Unicode Transformation Format 8-bit, or simply **UTF-8, is the current industry standard character encoding format**, as defined by the Unicode Standard, which was developed by the non-profit organization, Unicode Consortium in the 1990s. The UTF-8, UTF-16, and UTF-32 character encoding formats have all been published by the organization over the years.

In 2008, the UTF-8 HTML character encoding format was released. By 2019, it will be used on **more than 90 percent of all websites**. The World Web Consortium also recommends using it as the default HTML character encoding.

### HTML URL Encoding: Addressing Page Requests Efficiently

Since the internet can only understand the ASCII character set, **URL encoding is the golden rule of converting all non-ASCII characters** into readable or compatible characters.

Invalid ASCII characters are **replaced with a ” % ” sign** (without quotation mark), followed by two hexadecimal digits in the URL.  Spaces are considered invalid characters in URLs, in most cases, the HTML space encoding replaces a space with a plus (+) sign or with a %20 sign.

Thus, in HTML encoding UTF 8 plays a key role, and it is not case sensitive, you can type in any manner, just ensure it is there.

[CLICK ME](https://www.positioniseverything.net/html-encoding/)