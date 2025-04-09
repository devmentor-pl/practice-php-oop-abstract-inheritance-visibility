> :white_check_mark: *Jeśli będziesz mieć problem z rozwiązaniem tego zadania, poproś o pomoc na odpowiednim kanale na Slacku, tj. `s5e09-php-oop-abstract-inheritance-visibility` (dotyczy [mentee](https://devmentor.pl/mentoring-javascript/)) lub na ogólnodostępnej i bezpłatnej [społeczności na Discordzie](https://devmentor.pl/discord). Pamiętaj, aby treść Twojego wpisu spełniała [odpowiednie kryteria](https://devmentor.pl/jak-prosic-o-pomoc/).*

&nbsp;

# `#03` PHP & OOP (5-10): Abstract, Inheritance, Visibility

Polimorfizm to możliwość używania obiektów różnych klas przez ten sam interfejs lub typ nadrzędny. Pozwala pisać kod, który działa z wieloma typami obiektów w ten sam sposób.

Przyjmijmy, że implementujemy przeglądarkę internetową. Wiemy, że [drzewo DOM](https://kursjs.pl/kurs/dom/dom), zawiera wiele elementów HTML takich jak `div`, `p` czy `a`. Jak zbudować mechanizm, który będzie pozwalał wyświetlić dowolny element?

Może zdefiniować wspólną nazwę dla akcji "wyświetlania", a odpowiedzialność za implementację przerzucić na konkretny element?!

Twóim zdaniem będzie napisanie kodu, który umożliwi następujące działanie:

```
class Page {
    /**
    * @param HTMLElement[] $elements
    */
    public function render(array $elements): void {
        foreach ($elements as $element) {
           echo $element->render();
       }
    }
}

$div = new DivElement('Jakaś treść');
$p = new PElement('Jakiś tekst');
$a = new AElement('Jakiś link');

$elements = [
    $div,
    $p,
    $a,
];

$page = new Page();
$page->render($elements);
```



&nbsp;
> :no_entry: *Jeśli nie posiadasz materiałów do tego zadania tj. **Wideo**, znajdziesz je na stronie [laracasts.com](https://laracasts.com/referral/bogolubow)*

> :arrow_left: [*poprzednie zadanie*](./../02) | [*następne zadanie*](./../04) :arrow_right:
