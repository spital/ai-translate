# ai-translate

```python
text = '''Nowadays, the automatic translation will not amaze anyone,
but to see it work so easily and directly on my computer is still something amazing'''
for translate_pair in ['en>cs', 'cs>de', 'de>hu', 'hu>fi', 'fi>cs', 'cs>en']:
    source, target = translate_pair.split('>')
    tokenizer, model = load(f'Helsinki-NLP/opus-mt-{source}-{target}')
    translated = translate(text, model, tokenizer)
    print(f'{translate_pair}::{translated}')
    text = translated
```
en>cs::V současné době, automatický překlad nebude udivovat nikoho, ale vidět, že funguje tak snadno a přímo na mém počítači je stále něco úžasného

cs>de::Derzeit, eine automatische Übersetzung wird niemanden überraschen, aber zu sehen, dass es so einfach funktioniert und direkt auf meinem Computer ist immer noch etwas erstaunliches

de>hu::Jelenleg, egy automatikus fordítás nem fog meglepni senkit, de látni, hogy ez olyan egyszerű, és közvetlenül a számítógépemen még mindig valami elképesztő

hu>fi::Tällä hetkellä automaattinen käännös ei yllätä ketään, mutta näet, että se on niin yksinkertaista ja suoraan tietokoneellani on vielä jotain hämmästyttävää

fi>cs::V současné době automatický překlad nikoho nepřekvapí, ale vidíte, že je to tak jednoduché a přímo na mém počítači je stále něco úžasného

cs>en::At present, the automatic translation doesn't surprise anyone, but you can see that it's so simple and there's still something amazing on my computer.
