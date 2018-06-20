---
title: Speicherverwaltung in Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Arbeitsspeicher XLOPER12 [excel 2007], Verwalten von Arbeitsspeicher in Excel, Excel-Stapel Zeichenfolgen [Excel 2007], Verwalten von Arbeitsspeicher, Speicherverwaltung in Excel XLOPER Speicher [Excel 2007], Speicher [Excel 2007], Richtlinien für die Verwaltung
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 97c76d762fdc5e575c571804816e5581a7bec8bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790560"
---
# <a name="memory-management-in-excel"></a>Speicherverwaltung in Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beim Erstellen von effizienten und stabilen XLL-Dateien ist die Speicherverwaltung von zentraler Bedeutung. Wenn Speicher nicht korrekt verwaltet wird, kann dies zu einer Reihe von Problemen in Microsoft Excel führen – von kleineren Problemen, wie z. B. eine ineffiziente Speicherzuteilung und -initialisierung und kleinere Speicherverluste, bis hin zu größeren Problemen, wie z. B. eine Destabilisierung von Excel.
  
Eine fehlerhafte Verwaltung von Speicher ist die häufigste Ursache von schwerwiegenden Fehlern im Zusammenhang mit Add-Ins. Sie sollten daher Ihr Projekt mit einer konsistenten und gut durchdachten Strategie für Speicherverwaltung erstellen.  
  
Speicherverwaltung änderte komplexer in Microsoft Office Excel 2007 mit der Einführung von multithreaded Arbeitsmappe neu berechnen. Wenn Sie erstellen und threadsicheren Arbeitsblattfunktionen exportieren möchten, müssen Sie die resultierende Konflikte verwalten, die bei mehreren Threads für den Zugriff konkurrieren auftreten können.
  
Für die folgenden drei Datenstrukturtypen gibt es Überlegungen im Hinblick auf den Speicher:
  
- S **XLOPER**und **XLOPER12**s
    
- Zeichenfolgen, die nicht in einer **XLOPER** oder **XLOPER12** sind
    
- **FZ** und **FP12** arrays 
    
## <a name="xloperxloper12-memory"></a>XLOPER/XLOPER12-Speicher

Die **XLOPER**/ **XLOPER12** -Datenstruktur hat ein paar Untertypen, die Zeiger auf Blöcke mit Speicher, nämlich Zeichenfolgen (**XltypeStr**), Arrays (**XltypeMulti**) und externe Verweise (**XltypeRef**) enthalten. Beachten Sie außerdem, dass **XltypeMulti** Arrays Zeichenfolge **XLOPER**enthalten können/ **XLOPER12s** , die wiederum an andere Blöcke des Arbeitsspeichers zeigen. 
  
Ein **XLOPER**/ **XLOPER12** kann auf verschiedene Weise erstellt werden: 
  
- Von Excel bei der Vorbereitung von Argumenten, die an eine XLL-Funktion übergeben werden sollen
    
- Aufrufen von Excel bei der Rückgabe eines **XLOPER** oder **XLOPER12** in einer C-API 
    
- Von der DLL beim Erstellen von Argumenten, die an einen C-API-Aufruf übergeben werden sollen
    
- Von der DLL beim Erstellen eines Rückgabewerts einer XLL-Funktion
    
Ein Speicherblock innerhalb eines der auf den Speicher zeigenden Typen kann auf verschiedene Weise zugewiesen werden:
  
- Als statischer Block innerhalb Ihrer DLL außerhalb des Funktionscodes. In diesem Fall müssen Sie den Speicher nicht zuordnen oder freigeben.
    
- Als statischer Block innerhalb Ihrer DLL innerhalb eines Teils des Funktionscodes. In diesem Fall müssen Sie den Speicher nicht zuordnen oder freigeben.
    
- Es dynamisch belegt und von der DLL auf mehrere verschiedene Arten freigegeben werden kann: **Malloc** und **frei**, **neu** und **Löschen**und So weiter.
    
- Er kann dynamisch von Excel zugewiesen werden.
    
Angesichts der Anzahl von möglichen Herkunft für **XLOPER**/ **XLOPER12** Speicher und die Anzahl der Situationen, in denen die **XLOPER**/ **XLOPER12** diesen Speicher zugewiesen wurde, ist nicht verwunderlich, dass in diesem Thema kann scheinbar äußerst schwierig. Die Komplexität kann jedoch erheblich reduziert werden, wenn Sie mehrere Regeln und Richtlinien befolgen. 
  
### <a name="rules-for-working-with-xloperxloper12"></a>Regeln für das Arbeiten mit XLOPER/XLOPER12

- Versuchen Sie nicht, Speicher freigeben oder diese überschreiben soll **XLOPERs**/ **XLOPER12**s, die als Argumente an die XLL-Funktion übergeben werden. Sie sollten diese Argumente als schreibgeschützt behandeln. Weitere Informationen finden Sie unter "Zurückgeben von **XLOPER** oder **XLOPER12** durch Modifying Argumente direkten" unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
    
- Wenn Excel Speicher für eine **XLOPER**zugewiesen hat/ **XLOPER12** an die DLL in einem Aufruf der C-API zurückgegeben: 
    
  - Sie müssen den Speicher freigeben, wenn Sie die **XLOPER**nicht mehr benötigen/ **XLOPER12** mit einem Aufruf von [XlFree](xlfree.md). Verwenden Sie eine andere Methode, wie freien nicht, oder löschen Sie, um den Arbeitsspeicher freizugeben.
    
  - Ist der zurückgegebene Typ **XltypeMulti**, überschreiben alle **XLOPER**nicht/ **XLOPER12**s innerhalb des Arrays, insbesondere dann, wenn sie Zeichenfolgen, enthalten und insbesondere dann nicht, in dem Sie versuchen, mit einer Zeichenfolge zu überschreiben.
    
  - Wenn Sie die **XLOPER**zurückgeben möchten/ **XLOPER12** als Rückgabewert für die DLL-Funktion in Excel, müssen Sie Excel mitteilen, Speicher, mit der Excel freigegeben werden muss, wenn keine weiteren vorhanden ist. 
    
- Sie müssen ein **XLOPER**nur **XlFree** Aufrufen/ **XLOPER12** , die als den Rückgabewert in einer C-API-Aufruf erstellt wurde. 
    
- Wenn die DLL für eine **XLOPER**Speicher zugewiesen hat/ **XLOPER12** , die Sie als Rückgabewert für die DLL-Funktion in Excel zurückgeben möchten, müssen Sie Excel mitteilen, Speicher, die die DLL-Version muss vorhanden ist. 
    
### <a name="guidelines-for-memory-management"></a>Richtlinien für die Speicherverwaltung

- Achten Sie darauf, dass die DLL in der Methode, die Sie zum Zuteilen und Freigeben des Speichers verwenden, konsistent ist. Vermischen Sie keine Methoden. Ein guter Ansatz besteht darin, die verwendete Methode in einer Speicherklasse oder -struktur zu umschließen, in der Sie die verwendete Methode ändern können, ohne den Code an vielen Stellen zu verändern.
    
- Wenn Sie Arrays **XltypeMulti** innerhalb der DLL erstellen, wie Sie Speicher für Zeichenfolgen konsistent sein: immer dynamisch Speicher für sie oder verwenden Sie immer statischen Speicher. Wenn Sie so vorgehen, wenn Sie den Speicher freigegeben sind, wissen Sie, dass Sie immer oder nie die Zeichenfolgen freigeben müssen. 
    
- Kopieren Sie eine Excel erstellte **XLOPER**tiefe Kopien von Excel-reservierter Speicher treffen/ **XLOPER12**.
    
- Stellen Sie Excel zugeordneter Zeichenfolgen **XLOPER**nicht/ **XLOPER12**s in **XltypeMulti** Arrays. Tiefe Kopien der Zeichenfolgen und Zeiger auf die Kopien im Array gespeichert. 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Freigeben von Excel zugewiesenem XLOPER/XLOPER12-Arbeitsspeicher

Berücksichtigen Sie den folgenden XLL-Befehl, der **XlGetName** verwendet, um eine Zeichenfolge mit der Pfad und Dateiname der DLL zu erhalten und in ein Warnungsdialogfeld mit **XlcAlert**angezeigt.
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

Wenn die Funktion den Arbeitsspeicher auf den **xDllName**nicht mehr benötigt, können sie ihn durch den Aufruf der [XlFree-Funktion](xlfree.md), einer DLL-only C-API-Funktion frei. 
  
Die Funktion **XlFree** ist vollständig im Abschnitt Referenz Funktion dokumentiert (siehe [C-API-Funktionen, dass können werden aufgerufen, nur aus einer DLL oder XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), jedoch sollten Sie Folgendes beachten:
  
- Sie können an mehrere **XLOPER**Zeiger übergeben/ **XLOPER12**s in einem einzigen Aufruf zu **XlFree**, durch die Anzahl der Funktionsargumente in der ausgeführten Version von Excel (30 in Excel 2003 ab Excel 2007 255) unterstützt nur begrenzt.
    
- **XlFree** wird den darin enthaltenen Zeiger auf **NULL,** um sicherzustellen, dass einen Versuch, eine **XLOPER**frei/ **XLOPER12** , der bereits freigegeben wurde sicher ist. **XlFree** ist die einzige C-API-Funktion, die Argumente ändert. 
    
- Sie können für jede **XLOPER**sicher **XlFree** Aufrufen/ **XLOPER12** verwendet für den Rückgabewert für einen Aufruf der C-API, unabhängig davon, ob es sich um einen Zeiger auf den Speicher enthält. 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Zurückgeben von XLOPER/XLOPER12s, die von Excel freigegeben werden sollen

Angenommen Sie, Sie verwenden möchten, ändern den Befehl im Beispiel im vorherigen Abschnitt, und ändern Sie ihn in einer Tabellenfunktion, die den DLL Pfad und den Dateinamen ein, wenn ein **boolesches** **true** Argument und **#n/a** andernfalls übergeben zurückgibt. Sie können nicht deutlich **XlFree** , um die Zeichenfolge Arbeitsspeicher freizugeben, vor der Rückgabe an Excel aufrufen. Jedoch, wenn es nicht zu einem bestimmten Zeitpunkt freigegeben wird, wird das Add-in zu Speicherverlusten jedes Mal, wenn die Funktion aufgerufen wird. Um dieses Problem zu umgehen, lassen sich etwas in das Feld **Xltype** , der die **XLOPER**/ **XLOPER12**, als **XlbitXLFree** in xlcall.h definiert. Durch Festlegen dieser weist Excel an, dass er den zurückgegebenen Speicher freigeben muss, nachdem der Wert kopiert wird wurde. 
  
### <a name="example"></a>Beispiel

Im folgenden Codebeispiel ist der XLL-Befehl im vorherigen Abschnitt konvertiert in eine XLL-Arbeitsblattfunktion dargestellt.
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

XLL-Funktionen, mit denen **XLOPER**/ **XLOPER12**s muss als nutzen und Zurückgeben von Zeigern an **XLOPER**deklariert werden/ **XLOPER12**s. Die Verwendung in diesem Beispiel für eine statische **XLOPER12** innerhalb der Funktion ist nicht threadsicheren. Diese Funktion konnte nicht richtig registriert werden, als threadsicheren, aber riskieren Sie **xRtnValue** von einem Thread überschrieben wird, bevor ein anderer Thread mit diesem abgeschlossen wurde. 
  
Sie müssen nach dem Aufruf an den Excel-Rückruf **XlbitXLFree** festlegen, die es belegt. Wenn Sie dies vor der festlegen, wird überschrieben und verfügt nicht über den gewünschten Effekt. Wenn Sie beabsichtigen, den Wert vor der Rückgabe an das Arbeitsblatt als Argument eines Anrufs an eine andere C-API-Funktion zu verwenden, sollten Sie nach jedem solchen Aufruf dieses Bit festlegen. Andernfalls werden Sie Verwechseln Sie Funktionen, die nicht dieses Bit maskieren vor der Überprüfung der **XLOPER**/ **XLLOPER12** -Typ. 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>Zurückgeben von XLOPER/XLOPER12s, die von der DLL freigegeben werden sollen

Dadurch ein ähnliches Problem tritt auf, wenn Ihre XLL Speicher für eine **XLOPER**zugewiesen hat/ **XLOPER12** und möchte, dass sie nach Excel zurück. Excel erkennt einen anderen Bit, die im Feld **Xltype** , der die **XLOPER**festgelegt werden kann/ **XLOPER12**, als **XlbitDLLFree** in xlcall.h definiert. 
  
Wenn Excel **XLOPER**empfängt/ **XLOPER12** mit diesem bit gesetzt, wird versucht, eine Funktion aufgerufen, die durch die XLL aufgerufen [XlAutoFree](xlautofree-xlautofree12.md) (für **XLOPER**s) oder **xlAutoFree12** (für **XLOPER12**s) exportiert werden soll. Diese Funktion wird in der Funktionsreferenz zu ausführlicher beschrieben (siehe [Add-In - Manager und Schnittstelle XLL-Funktionen](add-in-manager-and-xll-interface-functions.md)), aber eine minimale beispielhafte wird hier angegeben. Es dient zum der **XLOPER**frei/ **XLOPER12** Arbeitsspeicher in eine Möglichkeit, die konsistent mit wie der ursprünglich zugeordnet ist. 
  
### <a name="examples"></a>Beispiele

Die folgende Beispielfunktion ist dieselbe wie die vorherige Funktion mit der Ausnahme, dass sie den Text enthält "der vollständige Pfadnamen für diese DLL ist" vor dem DLL-Namen.
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

Eine minimal ausreichende Implementierung der **xlAutoFree12** in die XLL, die die vorherige Funktion exportiert würde wie folgt aussehen. 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

Dieser Implementierung reicht nur, wenn die XLL nur **XLOPER12** Zeichenfolgen zurückgibt und diese Zeichenfolgen werden nur mit **Malloc**reserviert. Beachten Sie, dass der Test 
  
 ` if(p_oper->xltype == xltypeStr) `
  
würde in diesem Fall fehl, da **XlbitDLLFree** festgelegt ist. 
  
Im Allgemeinen sollten **XlAutoFree** und **xlAutoFree12** implementiert werden, damit sie Speicher XLL erstellt **XltypeMulti** Arrays und externe Verweise **XltypeRef** zugeordnet. 
  
Sie können Ihre XLL-Funktionen zu implementieren, sodass sie alle return dynamisch zugewiesen **XLOPER**s und **XLOPER12**s. In diesem Fall müssen Sie für alle solchen s **XLOPER**und **XLOPER12**s unabhängig von den Untertyp **XlbitDLLFree** festzulegen. Sie müssen auch **XlAutoFree** und **xlAutoFree12** implementieren, damit diese Speicher freigegeben wurde und außerdem alle Speicher auf den verwiesen wird innerhalb der **XLOPER**/ **XLOPER12**. Dieser Ansatz ist eine Möglichkeit, den Rückgabewert Thread sicher zu machen. Beispielsweise könnte die vorherige Funktion wie folgt umgeschrieben werden.
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

Weitere Informationen zu **XlAutoFree** und **xlAutoFree12**finden Sie unter [XlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).
  
## <a name="returning-modify-in-place-arguments"></a>Zurückgeben von Modify-in-Place-Argumenten

Excel ermöglicht einer XLL-Funktion, einen Wert durch Ändern eines vorhandenen Arguments zurückzugeben. Dies ist nur mit einem Argument möglich, das als Zeiger übergeben wird. Die Funktion muss hierfür so registriert werden, dass Excel weiß, welches Argument geändert wird.  
  
Diese Methode des Zurückgebens eines Werts wird für allen Datentypen unterstützt, die von einem Zeiger übergeben werden können, ist jedoch für die folgenden Typen besonders hilfreich:
  
- ASCII-Bytezeichenfolgen mit Längenzählung, die auf NULL enden
    
- Länge gezählt und Null endende Unicode-Zeichenfolgen (beginnend in Excel 2007)
    
- **FZ** Gleitkomma-arrays 
    
- **FP12** Gleitkomma-Arrays (beginnend in Excel 2007) 
    
> [!NOTE]
> Sie sollten nicht auf diese Weise **XLOPER**s oder **XLOPER12**s zurückzugeben. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md). 
  
Der Vorteil der Verwendung dieser Methode besteht darin, dass Excel den Speicher für Rückgabewerte zuweist, anstatt nur die return-Anweisung zu verwenden. Nachdem Excel das Lesen der zurückgegebenen Daten abgeschlossen hat, wird der Speicher freigegeben. Dadurch werden die Speicherverwaltungsaufgaben von der XLL-Funktion gelöst. Diese Technik ist threadsicher: Wenn Funktionen gleichzeitig von Excel in unterschiedlichen Threads aufgerufen werden, verfügt jeder Funktionsaufruf in jedem Thread über seinen eigenen Puffer.
  
Es ist hilfreich für die oben genannten Datentypen insbesondere, da der Mechanismus zum Rückrufen an die DLL, um Arbeitsspeicher freizugeben zurückzugeben, die nach dem existiert für **XLOPER**/ **XLOPER12**s existiert nicht für einfache Zeichenfolgen und **FZ** /  **FP12** Arrays. Daher müssen bei der Rückgabe erstellte DLL String oder Gleitkomma Array Sie die folgende Auswahl: 
  
- Legen Sie einen persistenten Zeiger auf einen dynamisch zugewiesenen Puffer fest, und geben Sie den Zeiger zurück. Führen Sie beim nächsten Aufruf der Funktion Folgendes aus: (1) Überprüfen Sie, dass der Zeiger nicht NULL ist. (2) Geben Sie die im vorherigen Aufruf zugewiesenen Ressourcen frei, und setzen Sie den Zeiger auf NULL zurück. (3) Verwenden Sie den Zeiger für einen neu zugewiesenen Speicherblock wieder.
    
- Erstellen Sie Ihre Zeichenfolgen und Arrays in einem statischen Puffer, der nicht freigegeben werden muss, und geben Sie einen Zeiger darauf zurück.
    
- Ändern Sie ein vorhandenes Argument, und schreiben Ihre Zeichenfolge oder Ihr Array direkt in den von Excel reservierten Platz.
    
Andernfalls müssen Sie ein **XLOPER**erstellen/ **XLOPER12**, und verwenden **XlbitDLLFree** und **XlAutoFree**/ **xlAutoFree12** , um die Ressourcen freizugeben. 
  
Die letzte Option möglicherweise die einfachste in diesen Fällen sein, in dem Sie ein Argument des gleichen Typs als Rückgabewert übergeben werden. Die wichtigsten wichtig ist, dass die Puffergrößen beschränkt sind, und Sie sehr achten, deren Überschreitung nicht. Erste dies falsche abstürzt Excel. Puffergrößen für Zeichenfolgen und **FZ**/ **FP12** Arrays werden als Nächstes erläutert. 
  
## <a name="strings"></a>Zeichenfolgen

Probleme mit der Verwaltung von Zeichenfolgenspeicher sind wohl die häufigste Ursache für Instabilität bei Anwendungen und Add-Ins. Dies ist angesichts der Vielzahl von Möglichkeiten zur Behandlung von Zeichenfolgen leicht nachvollziehbar: Zeichenfolgen mit NULL-Terminierung oder Längenzählung (oder beides), statische oder dynamische Puffer, Zeichenfolgen mit fester Länge oder fast unbegrenzter Länge, vom Betriebssystem verwalteter Speicher (z. B. OLE BSTR) oder nicht verwaltete Zeichenfolgen usw.
  
C/C++-Programmierer kennen sich am besten mit Zeichenfolgen aus, die auf NULL enden. Die standardmäßige C-Bibliothek wurde für derartige Zeichenfolgen entwickelt. Statische Zeichenfolgenliterale im Code werden Zeichenfolgen kompiliert, die auf NULL enden. Alternativ können in Excel Zeichenfolgen verwendet werden, die im Allgemeinen nicht auf NULL enden. Die Kombination dieser Fakten erfordert einen klaren und konsistenten Ansatz innerhalb Ihrer DLL/XLL im Hinblick auf die Behandlung von Zeichenfolgen und Zeichenfolgenspeicher.
  
Die häufigsten Probleme sind wie folgt:
  
- Die Übergabe von einen null oder ungültige Zeiger auf eine Funktion, die einen gültigen Zeiger erwartet und nicht der Fall ist oder der Mauszeiger Gültigkeit selbst kann nicht überprüft werden.
    
- Das Überschreiten der Grenzen eines Zeichenfolgenpuffers durch eine Funktion, die die Länge des Puffers nicht gegen die Länge der geschriebenen Zeichenfolge überprüfen kann.
    
- Der Versuch, Zeichenfolgenpufferspeicher freizugeben, der statisch ist oder bereits freigegeben wurde oder der auf eine Weise zugewiesen wurde, die nicht mit der Art und Weise konsistent ist, in der er freigegeben wurde.
    
- Speicherverluste, die daraus resultieren, dass Zeichenfolgen zugewiesen und dann nicht freigegeben werden, in der Regel in einer häufig aufgerufenen Funktion.
    
### <a name="rules-for-strings"></a>Regeln für Zeichenfolgen

Wie bei der **XLOPER**/ **XLOPER**s, Regeln und Sie befolgen Richtlinien vorhanden sind. Die Richtlinien sind die gleichen wie im vorherigen Abschnitt. Die Regeln hier sind eine Erweiterung der Regeln speziell für Zeichenfolgen.
  
 **Regeln:**
  
- Versuchen Sie nicht, Speicher freigeben oder diese überschreiben soll Zeichenfolge **XLOPER**/ **XLOPER12**s oder einfache Länge gezählt oder Null endende Zeichenfolgen als Argumente an die XLL-Funktion übergeben. Sie sollten diese Argumente als schreibgeschützt behandeln.
    
- Excel belegt, in dem Speicher für eine Zeichenfolge **XLOPER**/ **XLOPER12** für den Rückgabewert einer Rückruffunktion C-API **XlFree** verwenden, um es frei, oder **XlbitXLFree** festgelegt, wenn es in Excel aus eine XLL-Funktion zurückgeben. 
    
- In dem die DLL dynamisch weist eines Zeichenfolgenpuffers für eine **XLOPER**/ **XLOPER12**, es auf eine Weise konsistent mit, wie Sie zugewiesen, wenn Sie fertig oder **XlbitDLLFree** festgelegt, wenn es in Excel aus eine XLL-Funktion zurückgeben frei, und klicken Sie dann in freizugeben **xlAutoFree** /  **xlAutoFree12**.
    
- Wenn Excel Speicher für ein zurückgegebenes zur DLL in einem Aufruf der C-API **XltypeMulti** Array zugewiesen hat, eine beliebige Zeichenfolge **XLOPER**nicht überschreiben/ **XLOPER12**s innerhalb des Arrays. Solche Arrays müssen nur mit **XlFree**, freigegeben werden oder, wenn durch eine XLL-Funktion zurückgegeben wird, indem Sie **XlbitXLFree**festlegen.
    
### <a name="string-types-supported"></a>Unterstützte Zeichenfolgentypen

**C-API XltypeStr XLOPER/XLOPER12s**

|** Byte-Zeichenfolgen: ** XLOPER ***|** Breit Zeichenfolgen: ** XLOPER12 ***|
|:-----|:-----|
|Alle Versionen von Excel  <br/> |Starten in Excel 2007  <br/> |
|Max. Länge: 255 erweiterte ASCII-Bytes  <br/> |Maximale Länge 32.767 Unicode-Zeichen  <br/> |
|Erstes Byte (nicht signiert) = Länge  <br/> |Erstes Unicode-Zeichen = Länge  <br/> |
   
> [!IMPORTANT]
> Gehen Sie nicht null-Terminierung von **XLOPER** oder **XLOPER12** Zeichenfolgen. 
  
**C/C++-Zeichenfolgen**

|**Byte-Zeichenfolgen**|**Zeichenfolgen**|
|:-----|:-----|
|NULL endende (**Char** *) "C" die Maximallänge: 255 erweiterte ASCII-Bytes  <br/> |NULL endende (**Wchar_t** *) "C %" maximale Länge 32.767 Unicode-Zeichen  <br/> |
|Länge gezählt (**ohne Vorzeichen** *) "D"  <br/> |Länge gezählt (**Wchar_t** *) "D %"  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>Zeichenfolgen in xltypeMulti XLOPER/XLOPER12-Arrays

In vielen Fällen wird ein Array **XltypeMulti** für die Verwendung in Ihrer DLL/XLL in Excel erstellt. Einige Funktionen der XLM-Informationen zurückgeben solche Arrays. Beispielsweise gibt die C-API-Funktion **XlfGetWorkspace**, wenn das Argument *44* übergeben ein Array mit Zeichenfolgen, die derzeit registrierten DLL-Verfahren beschreiben. Der C-API-Funktion **XlfDialogBox** gibt eine geänderte Kopie der Array-Argument, das tiefe Kopien der Zeichenfolgen enthält. Möglicherweise ist am häufigsten eine XLL ein Array **XltypeMulti** stößt, an dem es als Argument an eine XLL-Funktion übergeben wurde, oder wurde aus einem Bereichsbezug in diesen Typ umgewandelt wurde. In diesen Fällen letzteren erstellt Excel tiefe Kopien von Zeichenfolgen in den Zellen der Datenquelle und verweist auf diese in das Array. 
  
Sie möchten diese Zeichenfolgen in der DLL zu ändern, sollten Sie eigene Tiefen Kopien erstellen. Wenn Sie Ihre eigene **XltypeMulti** Arrays erstellen, setzen Sie kein Excel zugeordneter Zeichenfolgen **XLOPER**/ **XLOPER12**s darin enthaltenen. Diese Risiken Sie nicht freigeben diese ordnungsgemäß später oder nicht in allen freigeben. Sie sollten erneut, tiefe Kopien der Zeichenfolgen und Zeiger auf die Kopien im Array gespeichert.
  
 **Beispiele**
  
Die folgende Beispielfunktion erstellt eine dynamisch zugeordnete Kopie einer Länge gezählt Unicode-Zeichenfolge. Beachten Sie, dass der Aufrufer letztlich in diesem Beispiel wird mit **Löschen**[] reservierten Speicher freigeben und beendet muss, dass die Source-Zeichenfolge nicht angenommen wird, null sein. Die Zeichenfolge Kopie abgeschnitten bei Bedarf für Sicherheit und ist nicht null beendet.
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

Diese Funktion kann dann sicher verwendet werden zum Kopieren von einer **XLOPER12**wie in der folgenden exportierbar XLL-Funktion dargestellt, die eine Kopie des Arguments zurückgibt, wenn es sich um eine Zeichenfolge handelt. Alle anderen Typen werden als eine leere Zeichenfolge zurückgegeben. Beachten Sie, dass die Bereiche nicht behandelt werden – gibt die Funktion **#VALUE!**. Die Funktion muss registriert werden, als ein Argument Type U nutzen, sodass Verweise als Werte übergeben werden. Dies ist gleichbedeutend mit der integrierten Arbeitsblattfunktion **T()** , mit der Ausnahme, dass **AsText** auch Fehler in leere Zeichenfolgen konvertiert. In diesem Codebeispiel wird vorausgesetzt, dass diese **xlAutoFree12** der Zeiger übergebenen und auch den Inhalt, der mithilfe des **Löschen**frei.
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a>Zurückgeben von Modify-in-Place-Zeichenfolgenargumenten

Argumente als Typen registriert, **F**, **G**, **F %** und **% G** direkt bearbeitet werden können. Wenn Excel Zeichenfolgenargumente für diese Typen vorbereitet wird, erstellt es einen Puffer maximale Länge. Klicken Sie dann kopiert zu übergebende Argumentzeichenfolge in, die, selbst wenn diese Zeichenfolge sehr wesentlich kürzer wird. Auf diese Weise können die XLL-Funktion, die ihren Rückgabewert direkt in den gleichen Arbeitsspeicher zu schreiben. 
  
Die Puffergößen für diese Typen sind wie folgt:
  
- **Byte-Zeichenfolgen:** 256 Byte, einschließlich der Leistungsindikator Länge (Typ G) oder Null-Beendigung (Typ F). 
    
- **Unicode-Zeichenfolgen:** 32.768 Breitzeichen (65.536 Byte) einschließlich der Leistungsindikator Länge (Typ G %) oder Null-Beendigung (Typ F %). 
    
> [!NOTE]
> Sie können eine solche Funktion nicht direkt aus VBA (Visual Basic für Applikationen) aufrufen, da Sie nicht sicherstellen können, dass ein ausreichend großer Puffer zugewiesen wurde. Sie können eine solche Funktion nur aus einer anderen DLL sicher aufrufen, wenn Sie explizit einen ausreichend großen Puffer übergeben haben. 
  
Hier ist ein Beispiel für eine XLL-Funktion, die übergebenen Null endende Breitzeichen Zeichenfolge mit der Standardbibliothek Funktion **Wcsrev**macht. Das Argument würde in diesem Fall als Typ **F %** erfasst werden.
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>Beständiger Speicher (binäre Namen)

Binäre Name definiert und zugeordnete Blöcke mit Binary, d. h., unstrukturierte, Daten, die zusammen mit der Arbeitsmappe gespeichert ist. Sie verwenden die Funktion [XlDefineBinaryName](xldefinebinaryname.md)erstellt werden, und die Daten werden mithilfe der Funktion [XlGetBinaryName](xlgetbinaryname.md)abgerufen. Beide Funktionen werden in der-Funktionsreferenz ausführlicher beschrieben (siehe [C-API-Funktionen, dass können werden aufgerufen, nur aus einer DLL oder XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), und beide verwenden **XltypeBigData** **XLOPER**/ **XLOPER12**. 
  
Informationen zu bekannten Problemen, die in der Praxis von binären Namen einschränken, finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
  
## <a name="excel-stack"></a>Excel-Stapel

Excel gibt seinen Stapelspeicher für alle geladenen DLLs frei. Der Stapelspeicher ist in der Regel für die einfache Verwendung mehr als ausreichend, und Sie müssen sich keine Gedanken darüber machen, solange Sie ein paar Richtlinien befolgen:  
  
- Übergeben Sie nicht sehr große Strukturen als Argumente an Funktionen nach dem Wert in dem Stapel. Übergeben Sie stattdessen Zeiger oder Verweise.
    
- Geben Sie keine große Strukturen an den Stapel zurück. Geben Sie Zeiger an statisch oder dynamisch zugewiesenen Speicher zurück, oder verwenden Sie Argumente, die als Verweis übergeben werden.
    
- Deklarieren Sie keine sehr großen automatischen Variablenstrukturen im Funktionscode. Deklarieren Sie sie ggf. als statisch.
    
- Rufen Sie Funktionen nicht rekursiv auf, es sei denn, Sie sind sicher, dass die Rekursionstiefe immer flach ist. Verwenden Sie stattdessen eine Schleife.
    
Wenn eine DLL wieder in Excel mithilfe der C-API aufruft, prüft Excel zunächst, ob genügend Speicherplatz vorhanden ist, auf dem Stapel für den ungünstigsten Fall Usage-Anruf, der hergestellt werden konnte. Wenn sie davon, dass möglicherweise nicht genügend Platz überzeugt, schlägt fehl den Anruf an sicheren, werden, obwohl es tatsächlich möglicherweise genügend Platz für dieses bestimmte Aufrufs wurden. In diesem Fall Zurückgeben der Rückrufe der Code **xlretFailed zurück**. Für die normale Verwendung der C-API und die Stack ist dies ein unwahrscheinlich Ursache des Fehlers eines Aufrufs C-API.
  
Wenn Sie betreffenden oder einfach neugierig sind oder Stack Speicherplatzmangel als einen Grund für ein Unerklärliches Fehler entfernen möchten, können Sie feststellen, mit einem Aufruf der Funktion [XlStack](xlstack.md) wie viel Speicherplatz vorhanden ist. 
  
## <a name="see-also"></a>Siehe auch



[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Multithreading und Arbeitsspeicher Konflikte in Excel](multithreading-and-memory-contention-in-excel.md)
  
[Entwickeln von Excel-XLLs](developing-excel-xlls.md)

