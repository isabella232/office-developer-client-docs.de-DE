---
title: Speicherverwaltung in Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Arbeitsspeicher xloper12 [excel 2007], Verwalten von Speicher in Excel, Excel-Stapel, Zeichenfolgen [Excel 2007], Speicherverwaltung, Speicherverwaltung in Excel, XLOPER-Speicher [Excel 2007], Speicher [Excel 2007], Richtlinien für die Verwaltung
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419541"
---
# <a name="memory-management-in-excel"></a>Speicherverwaltung in Excel

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beim Erstellen von effizienten und stabilen XLL-Dateien ist die Speicherverwaltung von zentraler Bedeutung. Wenn Speicher nicht korrekt verwaltet wird, kann dies zu einer Reihe von Problemen in Microsoft Excel führen – von kleineren Problemen, wie z. B. eine ineffiziente Speicherzuteilung und -initialisierung und kleinere Speicherverluste, bis hin zu größeren Problemen, wie z. B. eine Destabilisierung von Excel.
  
Eine fehlerhafte Verwaltung von Speicher ist die häufigste Ursache von schwerwiegenden Fehlern im Zusammenhang mit Add-Ins. Sie sollten daher Ihr Projekt mit einer konsistenten und gut durchdachten Strategie für Speicherverwaltung erstellen.  
  
Die Speicherverwaltung in Microsoft Office Excel 2007 wurde mit der Einführung der Multithreaded-Arbeitsmappenneuberechnung zunehmend komplexer. Wenn Sie threadsichere Arbeitsblattfunktionen erstellen und exportieren möchten, müssen Sie die Konflikte verwalten, die auftreten können, wenn mehrere Threads um Zugriff konkurrieren.
  
Für die folgenden drei Datenstrukturtypen gibt es Überlegungen im Hinblick auf den Speicher:
  
- **XLOPER** s und **XLOPER12** s
    
- Zeichenfolgen, die nicht in **XLOPER** oder **XLOPER12** enthalten sind
    
- **FP**- und **FP12**-Arrays 
    
## <a name="xloperxloper12-memory"></a>XLOPER/XLOPER12-Speicher

Die **XLOPER**/ **XLOPER12**-Datenstruktur weist einige Untertypen auf, die Zeiger auf Speicherblöcke enthalten, und zwar Zeichenfolgen (**xltypeStr**), Arrays (**xltypeMulti**) und externe Verweise (**xltypeRef**). Beachten Sie auch, dass **xltypeMulti**-Arrays die Zeichenfolgen **XLOPER**/ **XLOPER12s** enthalten können, die wiederum auf andere Speicherblöcke zeigen. 
  
Ein **XLOPER**/ **XLOPER12** kann auf verschiedene Arten erstellt werden: 
  
- Von Excel bei der Vorbereitung von Argumenten, die an eine XLL-Funktion übergeben werden sollen
    
- Von Excel beim Zurückgeben von **XLOPER** oder **XLOPER12** in einem C-API-Aufruf 
    
- Von der DLL beim Erstellen von Argumenten, die an einen C-API-Aufruf übergeben werden sollen
    
- Von der DLL beim Erstellen eines Rückgabewerts einer XLL-Funktion
    
Ein Speicherblock innerhalb eines der auf den Speicher zeigenden Typen kann auf verschiedene Weise zugewiesen werden:
  
- Als statischer Block innerhalb Ihrer DLL außerhalb des Funktionscodes. In diesem Fall müssen Sie den Speicher nicht zuordnen oder freigeben.
    
- Als statischer Block innerhalb Ihrer DLL innerhalb eines Teils des Funktionscodes. In diesem Fall müssen Sie den Speicher nicht zuordnen oder freigeben.
    
- Der Block kann dynamisch von der DLL auf verschiedene Weise zugeteilt und freigegeben werden: **malloc** und **free**, **new** und **delete** und so weiter.
    
- Er kann dynamisch von Excel zugewiesen werden.
    
Angesichts der Anzahl möglicher Ursprünge für **XLOPER**/ **XLOPER12**-Speicher und der Anzahl von Situationen, in denen der Speicher möglicherweise von **XLOPER**/ **XLOPER12** zugewiesen wurde, ist es nicht verwunderlich, dass dieses Thema sehr schwierig erscheinen mag. Die Komplexität kann jedoch erheblich verringert werden, wenn Sie mehrere Regeln und Richtlinien beachten. 
  
### <a name="rules-for-working-with-xloperxloper12"></a>Regeln für das Arbeiten mit XLOPER/XLOPER12

- Versuchen Sie nicht, Speicher freizugeben oder **XLOPERs**/ **XLOPER12** s zu überschreiben, die als Argumente an Ihre XLL-Funktion übergeben werden. Sie sollten diese Argumente als schreibgeschützt behandeln. Weitere Informationen finden Sie unter „Zurückgeben von **XLOPER** oder **XLOPER12** durch Ändern von vorhandenen Argumenten“ unter [Bekannte Probleme in Excel XLL Development](known-issues-in-excel-xll-development.md).
    
- Wenn Excel Speicher für ein **XLOPER**/ **XLOPER12** zugeteilt hat, das von Ihrer DLL in einem Aufruf der C-API zurückgegeben wurde: 
    
  - Sie müssen den Speicher durch einen Aufruf von [xlFree](xlfree.md) freigeben, wenn Sie **XLOPER**/ **XLOPER12** nicht mehr benötigen. Verwenden Sie keine andere Methode, z. B. „free“ oder „delete“, um den Speicher freizugeben.
    
  - Wenn der zurückgegebene Typ **xltypeMulti** ist, überschreiben Sie keine **XLOPER**/ **XLOPER12** s innerhalb des Arrays, insbesondere, wenn sie Zeichenfolgen enthalten, und vor allem nicht, wenn Sie das Überschreiben mit einer Zeichenfolge versuchen.
    
  - Wenn Sie **XLOPER**/ **XLOPER12** in Excel als Rückgabewert für die DLL-Funktion zurückgeben möchten, müssen Sie Excel anweisen, nach Abschluss des Vorgangs Speicherplatz freizugeben. 
    
- Sie müssen **xlFree** nur in einem **XLOPER**/ **XLOPER12** aufrufen, das als Rückgabewert für einen C-API-Aufruf erstellt wurde. 
    
- Wenn die DLL Speicher für ein **XLOPER**/ **XLOPER12** zugeteilt hat, das Sie in Excel als Rückgabewert für die DLL-Funktion zurückgeben möchten, müssen Sie Excel mitteilen, dass die DLL Speicherplatz freigeben muss.  
    
### <a name="guidelines-for-memory-management"></a>Richtlinien für die Speicherverwaltung

- Achten Sie darauf, dass die DLL in der Methode, die Sie zum Zuteilen und Freigeben des Speichers verwenden, konsistent ist. Vermischen Sie keine Methoden. Ein guter Ansatz besteht darin, die verwendete Methode in einer Speicherklasse oder -struktur zu umschließen, in der Sie die verwendete Methode ändern können, ohne den Code an vielen Stellen zu verändern.
    
- Bleiben Sie bei der Erstellung von **xltypeMulti**-Arrays innerhalb der DLL beim Zuteilen von Speicher für Zeichenfolgen konsistent: Teilen Sie den Speicher immer dynamisch zu, oder verwenden Sie immer statischen Speicher. Wenn Sie dies tun, wissen Sie beim Freigeben des Speichers, dass Sie die Zeichenfolgen immer oder nie freigeben müssen. 
    
- Erstellen Sie tiefe Kopien des Speichers, der Excel zugeteilt ist, wenn Sie ein in Excel erstelltes **XLOPER**/ **XLOPER12** kopieren.
    
- Setzen Sie die Excel zugeordnete Zeichenfolgen **XLOPER**/ **XLOPER12** s nicht in **XltypeMulti**-Arrays ein. Erstellen Sie tiefe Kopien der Zeichenfolgen, und speichern Sie Zeiger auf die Kopien im Array. 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a>Freigeben von Excel zugewiesenem XLOPER/XLOPER12-Arbeitsspeicher

Sehen Sie sich den folgenden XLL-Befehl an, der **xlGetName** zum Abrufen einer Zeichenfolge mit dem Pfad und Dateinamen der DLL verwendet und diese mit **xlcAlert** in einem Warnungsdialogfeld anzeigt.
  
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

Wenn die Funktion den Arbeitsspeicher, auf den von **xDllName** gezeigt wird, nicht mehr benötigt, kann dieser durch einen Aufruf der [xlFree-Funktion](xlfree.md), eine der C-API-Funktionen (nur DLL), freigegeben werden.  
  
Die **xlFree**-Funktion ist im Funktionsreferenzabschnitt ausführlich dokumentiert (siehe [C-API-Funktionen, die nur von einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), beachten Sie aber Folgendes:
  
- Sie können Zeiger an mehrere **XLOPER**/ **XLOPER12** s in einem einzigen Aufruf von **xlFree** übergeben. Dies wird nur durch die Anzahl der Funktionsargumente beschränkt, die in der ausgeführten Version von Excel unterstützt werden (30 in Excel 2003, 255 ab Excel 2007).
    
- **xlFree** legt den enthaltenen Zeiger auf **NULL** fest, um sicherzustellen, dass der Versuch, ein **XLOPER**/ **XLOPER12**, das bereits freigegeben wurde, freizugeben, sicher ist. **XlFree** ist die einzige C-API-Funktion, die die zugehörigen Argumente ändert. 
    
- Sie können problemlos **xlFree** in allen **XLOPER**/ **XLOPER12** aufrufen, die für den Rückgabewert eines Aufrufs der C-API verwendet werden, unabhängig davon, ob ein Zeiger auf Speicher darin enthalten ist. 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a>Zurückgeben von XLOPER/XLOPER12s, die von Excel freigegeben werden sollen

Angenommen, Sie möchten den Beispielbefehl im vorherigen Abschnitt bearbeiten und in eine Arbeitsblattfunktion ändern, die den DLL-Pfad und den Dateinamen zurückgibt, wenn ein **Boolean** **true**-Argument übergeben wird, andernfalls **#N/A**. Sie können natürlich **xlFree** nicht aufrufen, um den Zeichenfolgenspeicher vor der Rückgabe an Excel freizugeben. Wenn der Speicher jedoch nicht irgendwann freigegeben wird, geht bei dem Add-In bei jedem Aufruf der Funktion Speicher verloren. Um dieses Problem zu umgehen, können Sie ein Bit im **xltype**-Feld von **XLOPER**/ **XLOPER12**, definiert als **xlbitXLFree** in „xlcall.h“ festlegen. Wenn dies festgelegt wird, wird Excel angewiesen, den zurückgegebenen Speicher freizugeben, wenn das Kopieren des Werts abgeschlossen ist. 
  
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

XLL-Funktionen, die **XLOPER**/ **XLOPER12** s verwenden, müssen als Zeiger auf **XLOPER**/ **XLOPER12** s deklariert werden. Die Verwendung in diesem Beispiel eines statischen **XLOPER12** innerhalb der Funktion ist nicht threadsicher. Sie könnten diese Funktion fälschlicherweise als threadsicher registrieren, würden jedoch riskieren, dass **xRtnValue** von einem Thread überschrieben wird, bevor ein anderer Thread damit fertig ist. 
  
Sie müssen **xlbitXLFree** nach dem Aufruf des Excel-Rückrufs festlegen, der dies zuweist. Wenn Sie dies davor festlegen, wird es überschrieben und hat nicht den gewünschten Effekt. Wenn Sie beabsichtigen, den Wert vor der Rückgabe an das Arbeitsblatt als Argument in einem Aufruf einer anderen C-API-Funktion zu verwenden, sollten Sie dieses Bit nach einem derartigen Aufruf festlegen. Andernfalls könnten Sie Funktionen verwechseln, die dieses Bit nicht maskieren, bevor der **XLOPER**/ **XLLOPER12**-Typ überprüft wird. 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a>Zurückgeben von XLOPER/XLOPER12s, die von der DLL freigegeben werden sollen

Ein ähnliches Problem tritt auf, wenn Ihre XLL Speicher für ein **XLOPER**/ **XLOPER12** zugewiesen hat und diesen an Excel zurückgeben möchte. Excel erkennt ein anderes Bit, das im **xltype**-Feld von **XLOPER**/ **XLOPER12**, definiert als **xlbitDLLFree** in xlcall.h, festgelegt werden kann. 
  
Wenn Excel **XLOPER**/ **XLOPER12** erhält, wobei dieses Bit festgelegt ist, versucht es, eine Funktion aufzurufen, die von der XLL mit dem Namen [xlAutoFree](xlautofree-xlautofree12.md) (für **XLOPER** s) oder **xlAutoFree12** (für **XLOPER12** s) exportiert werden sollte. Diese Funktion wird in der Funktionsreferenz ausführlicher beschrieben (siehe [-Add-In-Manager und XLL-Schnittstellenfunktionen](add-in-manager-and-xll-interface-functions.md)). Hier finden Sie aber eine beispielhafte minimale Implementierung. Ihr Zweck besteht darin, den **XLOPER**/ **XLOPER12**-Speicher auf eine Weise freizugeben, die mit der ursprünglichen Zuweisung konsistent ist. 
  
### <a name="examples"></a>Beispiele

Die folgende Beispielfunktion hat den gleichen Zweck wie die vorherige Funktion, mit der Ausnahme, dass sie den Text „Der vollständige Pfadname für diese DLL ist“ vor dem DLL-Namen umfasst.
  
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

Eine minimal hinreichende Implementierung von **xlAutoFree12** in der XLL, die die vorherige Funktion exportiert hat, wäre wie folgt. 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

Diese Implementierung ist nur ausreichend, wenn die XLL nur **XLOPER12**-Zeichenfolgen zurückgibt und diese Zeichenfolgen nur mithilfe von **malloc** zugewiesen werden. Beachten Sie, dass bei dem Test  
  
 ` if(p_oper->xltype == xltypeStr) `
  
in diesem Fall ein Fehler auftreten würde, da **xlbitDLLFree** festgelegt ist. 
  
Im Allgemeinen sollten **xlAutoFree** und **xlAutoFree12** so implementiert werden, dass Speicherplatz freigegeben wird, der von XLL erstellten **xltypeMulti**-Arrays und externen **xltypeRef**-Referenzen zugewiesen ist. 
  
Vielleicht entschließen Sie sich, Ihre XLL-Funktionen so zu implementieren, dass sie ALLE dynamisch zugewiesenen **XLOPER** s und **XLOPER12** s zurückgeben. In diesem Fall müssen Sie **xlbitDLLFree** für alle **XLOPER** s und **XLOPER12** s unabhängig von den Untertypen festlegen. Außerdem müssten Sie **xlAutoFree** und **xlAutoFree12** implementieren, damit dieser Speicher und auch der gesamte Speicher, auf den innerhalb der **XLOPER**/ **XLOPER12** gezeigt wird, freigegeben wird. Dieser Ansatz ist eine Möglichkeit, um den Rückgabewert threadsicher zu machen. Die vorherige Funktion könnte z. B. wie folgt umgeschrieben werden.
  
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

Weitere Informationen zu **xlAutoFree** und **xlAutoFree12** finden Sie unter [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).
  
## <a name="returning-modify-in-place-arguments"></a>Zurückgeben von Modify-in-Place-Argumenten

Excel ermöglicht einer XLL-Funktion, einen Wert durch Ändern eines vorhandenen Arguments zurückzugeben. Dies ist nur mit einem Argument möglich, das als Zeiger übergeben wird. Die Funktion muss hierfür so registriert werden, dass Excel weiß, welches Argument geändert wird.  
  
Diese Methode des Zurückgebens eines Werts wird für allen Datentypen unterstützt, die von einem Zeiger übergeben werden können, ist jedoch für die folgenden Typen besonders hilfreich:
  
- ASCII-Bytezeichenfolgen mit Längenzählung, die auf NULL enden
    
- Unicode-Zeichenfolgen für Breitzeichen mit Längenzählung, die auf NULL enden (beginnend bei Excel 2007)
    
- **FP**-Gleitkommaarrays 
    
- **FP12**-Gleitkommaarrays (beginnend bei Excel 2007) 
    
> [!NOTE]
> Sie sollten nicht versuchen, **XLOPER** s oder **XLOPER12** s auf diese Weise zurückzugeben. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md). 
  
Der Vorteil der Verwendung dieser Methode besteht darin, dass Excel den Speicher für Rückgabewerte zuweist, anstatt nur die return-Anweisung zu verwenden. Nachdem Excel das Lesen der zurückgegebenen Daten abgeschlossen hat, wird der Speicher freigegeben. Dadurch werden die Speicherverwaltungsaufgaben von der XLL-Funktion gelöst. Diese Technik ist threadsicher: Wenn Funktionen gleichzeitig von Excel in unterschiedlichen Threads aufgerufen werden, verfügt jeder Funktionsaufruf in jedem Thread über seinen eigenen Puffer.
  
Dies ist besonders für die zuvor aufgeführten Datentypen hilfreich, da der Mechanismus für den Rückruf der DLL zum Freigeben von Speicher nach der Rückgabe, der für **XLOPER**/ **XLOPER12** s besteht, für einfache Zeichenfolgen und **FP**/ **FP12**-Arrays nicht vorhanden ist. Daher stehen Ihnen beim Zurückgeben einer von DLL erstellten Zeichenfolge oder eines Gleitkommaarrays die folgenden Optionen zur Verfügung: 
  
- Legen Sie einen persistenten Zeiger auf einen dynamisch zugewiesenen Puffer fest, und geben Sie den Zeiger zurück. Führen Sie beim nächsten Aufruf der Funktion Folgendes aus: (1) Überprüfen Sie, dass der Zeiger nicht NULL ist. (2) Geben Sie die im vorherigen Aufruf zugewiesenen Ressourcen frei, und setzen Sie den Zeiger auf NULL zurück. (3) Verwenden Sie den Zeiger für einen neu zugewiesenen Speicherblock wieder.
    
- Erstellen Sie Ihre Zeichenfolgen und Arrays in einem statischen Puffer, der nicht freigegeben werden muss, und geben Sie einen Zeiger darauf zurück.
    
- Ändern Sie ein vorhandenes Argument, und schreiben Ihre Zeichenfolge oder Ihr Array direkt in den von Excel reservierten Platz.
    
Andernfalls müssen Sie ein **XLOPER**/ **XLOPER12** erstellen und **xlbitDLLFree** und **xlAutoFree**/ **xlAutoFree12** verwenden, um die Ressourcen freizugeben. 
  
Die letzte Option ist die einfachste Lösung, wenn ein Argument mit demselben Typ wie der Rückgabewert an Sie übergeben wird. Wichtig ist hierbei, dass Sie beachten, dass die Puffergrößen beschränkt sind und Sie sehr vorsichtig sein müssen, um diese nicht zu überschreiten. Wenn dies passiert, kann Excel abstürzen. Als Nächstes werden Puffergrößen für Zeichenfolgen und **FP**/ **FP12**-Arrays erläutert. 
  
## <a name="strings"></a>Strings

Probleme mit der Verwaltung von Zeichenfolgenspeicher sind wohl die häufigste Ursache für Instabilität bei Anwendungen und Add-Ins. Dies ist angesichts der Vielzahl von Möglichkeiten zur Behandlung von Zeichenfolgen leicht nachvollziehbar: Zeichenfolgen mit NULL-Terminierung oder Längenzählung (oder beides), statische oder dynamische Puffer, Zeichenfolgen mit fester Länge oder fast unbegrenzter Länge, vom Betriebssystem verwalteter Speicher (z. B. OLE BSTR) oder nicht verwaltete Zeichenfolgen usw.
  
C/C++-Programmierer kennen sich am besten mit Zeichenfolgen aus, die auf NULL enden. Die standardmäßige C-Bibliothek wurde für derartige Zeichenfolgen entwickelt. Statische Zeichenfolgenliterale im Code werden Zeichenfolgen kompiliert, die auf NULL enden. Alternativ können in Excel Zeichenfolgen verwendet werden, die im Allgemeinen nicht auf NULL enden. Die Kombination dieser Fakten erfordert einen klaren und konsistenten Ansatz innerhalb Ihrer DLL/XLL im Hinblick auf die Behandlung von Zeichenfolgen und Zeichenfolgenspeicher.
  
Die häufigsten Probleme sind wie folgt:
  
- Die Übergabe eines NULL-Zeigers oder eines ungültigen Zeigers an eine Funktion, die einen gültigen Zeiger erwartet und die die Gültigkeit des Zeigers nicht selbst überprüft bzw. überprüfen kann.
    
- Das Überschreiten der Grenzen eines Zeichenfolgenpuffers durch eine Funktion, die die Länge des Puffers nicht gegen die Länge der geschriebenen Zeichenfolge überprüfen kann.
    
- Der Versuch, Zeichenfolgenpufferspeicher freizugeben, der statisch ist oder bereits freigegeben wurde oder der auf eine Weise zugewiesen wurde, die nicht mit der Art und Weise konsistent ist, in der er freigegeben wurde.
    
- Speicherverluste, die daraus resultieren, dass Zeichenfolgen zugewiesen und dann nicht freigegeben werden, in der Regel in einer häufig aufgerufenen Funktion.
    
### <a name="rules-for-strings"></a>Regeln für Zeichenfolgen

Wie bei **XLOPER**/ **XLOPER** s gibt es Regeln und Richtlinien, die Sie beachten sollten. Die Richtlinien sind identisch mit denen im vorherigen Abschnitt. Die folgenden Regeln sind eine Erweiterung der Regeln, die speziell für Zeichenfolgen gelten.
  
 **Regeln:**
  
- Versuchen Sie nicht, Speicher freizugeben oder Zeichenfolgen-**XLOPER**/ **XLOPER12** s bzw. einfache Zeichenfolgen mit Längenzählung oder NULL-Terminierung zu überschreiben, die als Argumente an Ihre XLL-Funktion übergeben werden. Sie sollten diese Argumente als schreibgeschützt behandeln.
    
- Wenn Excel Speicher für ein Zeichenfolgen-**XLOPER**/ **XLOPER12** für den Rückgabewert einer C-API-Rückruffunktion zuweist, verwenden Sie **xlFree**, um diesen freizugeben, oder legen Sie **xlbitXLFree** fest, wenn Sie ihn aus einer XLL-Funktion an Excel zurückgeben möchten. 
    
- Wenn die DLL einen Zeichenfolgenpuffer dynamisch für ein **XLOPER**/ **XLOPER12** zuweist, geben Sie diesen auf eine Art und Weise frei, die damit konsistent ist, wie er nach Abschluss zugewiesen wurde, oder legen Sie **xlbitDLLFree** fest, wenn Sie ihn aus einer XLL-Funktion an Excel zurückgeben möchten, und geben Sie ihn dann in **xlAutoFree**/ **xlAutoFree12** frei.
    
- Wenn Excel Speicher für ein **xltypeMulti**-Array zugewiesen hat, der in einem Aufruf der C-API an Ihre DLL zurückgegeben wird, überschreiben Sie keine Zeichenfolgen-**XLOPER**/ **XLOPER12** s innerhalb des Arrays. Solche Arrays dürfen nur mithilfe von **xlFree** freigegeben werden, oder durch Festlegen von **xlbitXLFree**, wenn sie von einer XLL-Funktion zurückgegeben werden.
    
### <a name="string-types-supported"></a>Unterstützte Zeichenfolgentypen

**xltypeStr XLOPER/XLOPER12s von C-API**

|**Bytezeichenfolgen: **XLOPER****|**Zeichenfolgen für Breitzeichen: ** XLOPER12****|
|:-----|:-----|
|Alle Versionen von Excel  <br/> |Ab Excel 2007  <br/> |
|Maximale Länge: 255 erweiterte ASCII-Bytes  <br/> |Maximale Länge 32.767 Unicode-Zeichen  <br/> |
|Erstes Byte (nicht signiert) = Länge  <br/> |Erstes Unicode-Zeichen = Länge  <br/> |
   
> [!IMPORTANT]
> Gehen Sie nicht davon aus, dass **XLOPER**- oder **XLOPER12**-Zeichenfolgen auf NULL enden. 
  
**C/C++-Zeichenfolgen**

|**Bytezeichenfolgen**|**Zeichenfolgen für Breitzeichen**|
|:-----|:-----|
|Null-Terminierung (**Zeichen** *) "C" Maximale Länge: 255 erweiterte ASCII-Bytes  <br/> |Null-Terminierung (**wchar_t** *) "C%" Maximale Länge 32.767 Unicode-Zeichen  <br/> |
|Längenzählung (**nicht signiertes Zeichen** *) "D"  <br/> |Längenzählung (**wchar_t** *) "D%"  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a>Zeichenfolgen in xltypeMulti XLOPER/XLOPER12-Arrays

In vielen Fällen erstellt Excel ein **xltypeMulti**-Array zur Verwendung in Ihrer DLL/XLL. Einige der XLM-Informationsfunktionen geben solche Arrays zurück. Die C-API-Funktion **xlfGetWorkspace** gibt beispielsweise ein Array mit Zeichenfolgen zurück, die alle die derzeit registrierten DLL-Prozeduren beschreiben, wenn das Argument *44* übergeben wird. Die C-API-Funktion **xlfDialogBox** gibt eine geänderte Kopie ihres Arrayarguments zurück, das tiefe Kopien der Zeichenfolgen enthält. Am häufigsten trifft eine XLL auf ein **xltypeMulti**-Array, wo ein Argument an eine XLL-Funktion übergeben wurde, oder dieser Typ wurde ihr von einem Bereichsbezug aufgezwungen. In diesen Fällen erstellt Excel tiefe Kopien der Zeichenfolgen in den Quellzellen und zeigt innerhalb des Arrays auf diese. 
  
Wenn Sie diese Zeichenfolgen in Ihrer DLL ändern möchten, sollten Sie Ihre eigenen tiefen Kopien erstellen. Wenn Sie eigene **xltypeMulti**-Arrays erstellen, platzieren Sie keine von Excel zugewiesenen Zeichenfolgen-**XLOPER**/ **XLOPER12** s darin. Auf diese Weise besteht das Risiko, dass Sie sie später nicht korrekt oder gar nicht freigeben. Sie sollten erneut tiefe Kopien der Zeichenfolgen erstellen und Zeiger auf die Kopien im Array speichern.
  
 **Beispiele**
  
Die folgende Beispielfunktion erstellt eine dynamisch zugewiesene Kopie einer Unicode-Länge mit Längenbeschränkung. Beachten Sie, dass der Aufrufer letztendlich den in diesem Beispiel zugewiesenen Speicher mithilfe von **delete**[] freigeben muss und dass für die Quellzeichenfolge keine Null-Terminierung angenommen wird. Die kopierte Zeichenfolge wird aus Sicherheitsgründen abgeschnitten und endet nicht auf NULL.
  
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

Diese Funktion kann dann sicher zum Kopieren einer **XLOPER12** verwendet werden, wie in der folgenden exportierbaren XLL-Funktion dargestellt, die eine Kopie ihrer Argumente zurückgibt, wenn es sich um eine Zeichenfolge handelt. Alle anderen Typen werden als eine Zeichenfolge der Länge Null zurückgegeben. Beachten Sie, dass Bereiche nicht verarbeitet werden, die Funktion gibt **#VALUE!** zurück. Die Funktion muss so registriert werden, dass sie ein Argument vom Typ U verwendet, damit Verweise als Werte übergeben werden. Dies entspricht der integrierten Arbeitsblattfunktion **T()**, mit der Ausnahme, dass **AsText** auch Fehler in leere Zeichenfolgen konvertiert. In diesem Codebeispiel wird vorausgesetzt, dass **xlAutoFree12** den übergebenen Zeiger und auch dessen Inhalt mithilfe von **delete** freigibt.
  
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

Argumente, die als die Typen **F**, **G**, **F%** und **G%** registriert sind, können direkt bearbeitet werden. Wenn Excel Zeichenfolgenargumente für diese Typen vorbereitet, wird ein Puffer mit maximaler Länge erstellt. Dann wir die Argumentzeichenfolge in den Puffer kopiert, auch wenn diese Zeichenfolge viel kürzer ist. Auf diese Weise kann die XLL- ihren Rückgabewert direkt in den gleichen Speicher schreiben. 
  
Die Puffergößen für diese Typen sind wie folgt:
  
- **Bytezeichenfolgen:** 256 Bytes, einschließlich der Längenzählung (Typ G) oder Null-Terminierung (Typ F). 
    
- **Unicode-Zeichenfolgen:** 32.768 Breitzeichen (65.536 Bytes), einschließlich der Längenzählung (Typ G%) oder Null-Terminierung (Typ F%). 
    
> [!NOTE]
> Sie können eine solche Funktion nicht direkt aus VBA (Visual Basic für Applikationen) aufrufen, da Sie nicht sicherstellen können, dass ein ausreichend großer Puffer zugewiesen wurde. Sie können eine solche Funktion nur aus einer anderen DLL sicher aufrufen, wenn Sie explizit einen ausreichend großen Puffer übergeben haben. 
  
Nachfolgend sehen Sie ein Beispiel für eine XLL-Funktion, die ein übergebenes, auf NULL endendes Breitzeichen mithilfe der standardmäßigen Bibliotheksfunktion **wcsrev** reserviert. Das Argument würde in diesem Fall als Typ **F%** registriert.
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a>Beständiger Speicher (binäre Namen)

Binäre Namen werden mit Blöcken von Binärdaten definiert und zugeordnet, d. h., unstrukturierte Daten, die zusammen mit der Arbeitsmappe gespeichert werden. Sie werden mit der Funktion [xlDefineBinaryName](xldefinebinaryname.md) erstellt, und die Daten werden mit der Funktion [xlGetBinaryName](xlgetbinaryname.md) abgerufen. Beide Funktionen werden in der Funktionsreferenz ausführlicher beschrieben (siehe [C-API-Funktionen, die nur von einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), und beide verwenden **xltypeBigData** **XLOPER**/ **XLOPER12**. 
  
Weitere Informationen zu bekannten Problemen, durch die die praktischen Anwendungen von binären Namen eingeschränkt werden, finden Sie unter [Bekannte Probleme in Excel XLL Development](known-issues-in-excel-xll-development.md).
  
## <a name="excel-stack"></a>Excel-Stapel

Excel gibt seinen Stapelspeicher für alle geladenen DLLs frei. Der Stapelspeicher ist in der Regel für die einfache Verwendung mehr als ausreichend, und Sie müssen sich keine Gedanken darüber machen, solange Sie ein paar Richtlinien befolgen:  
  
- Übergeben Sie nicht sehr große Strukturen als Argumente an Funktionen nach dem Wert in dem Stapel. Übergeben Sie stattdessen Zeiger oder Verweise.
    
- Geben Sie keine große Strukturen an den Stapel zurück. Geben Sie Zeiger an statisch oder dynamisch zugewiesenen Speicher zurück, oder verwenden Sie Argumente, die als Verweis übergeben werden.
    
- Deklarieren Sie keine sehr großen automatischen Variablenstrukturen im Funktionscode. Deklarieren Sie sie ggf. als statisch.
    
- Rufen Sie Funktionen nicht rekursiv auf, es sei denn, Sie sind sicher, dass die Rekursionstiefe immer flach ist. Versuchen Sie es stattdessen mit einer Schleife.
    
Wenn eine DLL-Datei einen Rückruf in Excel mithilfe der C-API unternimmt, überprüft Excel zuerst, ob genügend Speicherplatz auf dem Stapel für den Aufruf mit der größten Nutzung vorhanden ist. Wenn Excel denkt, dass möglicherweise nicht genügend Platz vorhanden ist tritt ein Fehler bei dem Aufruf auf, auch wenn möglicherweise ausreichend Speicherplatz für diesen bestimmten Anruf vorhanden gewesen wäre. In diesem Fall gibt der Rückruf den Code **xlretFailed** zurück. Für eine normale Verwendung der C-API und des Stapels ist dies eine unwahrscheinliche Ursache für den Fehler eines C-API-Aufrufs.
  
Wenn Sie sich Sorgen über den Stapelspeicher machen oder einfach nur neugierig sind oder vielleicht den mangelnden Stapelspeicher als Ursache für einen unerklärlichen Fehler beheben möchten, können Sie herausfinden, wie viel Stapelspeicher vorhanden ist, indem Sie die Funktion [xlStack](xlstack.md) aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[Multithread-Neuberechnung in Excel](multithreaded-recalculation-in-excel.md)
  
[Multithreading und Speicherkonflikte in Excel](multithreading-and-memory-contention-in-excel.md)
  
[Entwickeln von XLLs für Excel](developing-excel-xlls.md)

