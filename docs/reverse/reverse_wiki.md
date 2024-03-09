# Od czego zacząć analizę pliku?
1. `file <nazwa_pliku>` - odpowie nam na pytanie, jaki mamy format pliku wykonywalnego 
( **PE** - Windows, **ELF** - Linux) oraz na jaką architekturę został stworzony (32 lub 64-bitową).
2. `strings <nazwa_pliku>` - wyświetli nam wszystkie ciągi znaków drukowalnych (ang. printable characters) znajdujące się w analizowanym pliku: możemy tam znaleźć np. komunikaty wyświetlane użytkownikowi w trakcie działania programu (a czasami nawet flagę).
# Dekompilacja:
[GHIDRA](https://ghidra-sre.org/) - stosunkowo proste w obsłudze, a zarazem bardzo potężne narzędzie pozwalające nam "wyciągnąć" z pliku kod źródłowy zarówno w formie instrukcji assemblerowych jak i zdekompilowanego kodu w języku C.
 
 [dnSpy](https://github.com/dnSpy/dnSpy) - pozwala na dekompilację programów napisanych na platformę **.NET**. Oprócz samego podglądania kodu źródłowego pozwala na edytowanie klas oraz metod, a następnie rekompiluje program, uwzględniając dokonane przez nas zmiany.
 
## Analiza "ELFów":
1. `ltrace <nazwa_pliku> [argumenty]` - podczas wykonywania programu zostaną wyświetlone informacje o tym, jakie funkcje biblioteczne (i z jakimi argumentami) zostają wywoływane w trakcie działania programu.
2.  `strace <nazwa_pliku> [argumenty]` - podobnie jak wyżej, tylko dostajemy informacje o funkcjach systemowych
3. `gdb --args <nazwa_pliku> [argumenty]` - gdb to popularny debugger, jego "goła" wersja nie jest zbyt przyjazna, jednak pluginy, takie jak [pwndbg](https://github.com/pwndbg/pwndbg) lub [GEF](https://github.com/hugsy/gef), pozwalają po odrobinie praktyki na swobodne poruszanie się po analizowanych programach.

## Analiza PE:
x64dbg/x32dbg [LINK](https://x64dbg.com/) - debugger na system Windows, w odróżnieniu od gdb posiada GUI.