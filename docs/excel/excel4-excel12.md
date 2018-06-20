---
title: Excel4/Excel12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12
- Excel4
keywords:
- Excel4-Funktion [excel 2007], Excel12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1c2c775cc7c5b051e4a1381df09ef29e79e2aca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790490"
---
# <a name="excel4excel12"></a>Excel4/Excel12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft einen internen Microsoft Excel-Arbeitsblatt-Funktion, Blatt Makrofunktion oder Befehls, oder XLL-only Sonderfunktion bzw., aus innerhalb einer DLL/XLL oder Code-Ressource.
  
Alle aktuelle Versionen von Excel unterstützen **Excel4**. Ab Excel 2007 wird **Excel12** unterstützt. 
  
Nur, wenn Excel Steuerelement an die DLL oder XLL übergeben wurde, können diese Funktionen aufgerufen werden. Sie können auch aufgerufen werden, wenn Excel Steuerelement indirekt über einen Aufruf zu Visual Basic für Applikationen (VBA) übergeben wurde. Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden. Beispielsweise können nicht sie während des Aufrufs der [DllMain](http://msdn.microsoft.com/library/base.dllmain%28Office.15%29.aspx) -Funktion oder in anderen Fällen aufgerufen werden, wenn das Betriebssystem die DLL aufgerufen hat, oder aus einem Thread erstellt, die von der DLL. 
  
Die Funktionen [Excel4v und Excel12v](excel4v-excel12v.md) annehmen deren Argumente als ein Array, während die Funktionen **Excel4** und **Excel12** deren Argumente als Liste variabler Länge auf dem Stapel annehmen. In jeder anderen Hinsicht **Excel4** verhält sich wie **Excel4v**und **Excel12** verhält sich **Excel12v**identisch.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**Int**)
  
Eine Zahl, die den Befehl, Function- oder Sonderfunktion gibt an, die Sie anrufen möchten. Eine Liste der gültigen _iFunction_ Werte finden Sie unter den folgenden Hinweisen. 
  
 _pxRes_ (**LPXLOPER** oder **LPXLOPER12**)
  
Ein Zeiger auf eine **XLOPER** (mit **Excel4**) oder ein **XLOPER12** (mit **Excel12**), die das Ergebnis der ausgewertete Funktion enthalten soll.
  
 _iCount_ (**Int**)
  
Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden. In Versionen von Excel bis 2003 zu kann dies eine beliebige Zahl von 0 bis 30 sein. Ab Excel 2007, kann dies eine beliebige Zahl zwischen 0 und 255 sein.
  
 _argument1..._ (**LPXLOPER** oder **LPXLOPER12**)
  
Die optionalen Argumente an die Funktion. Alle Argumente müssen Zeiger auf **XLOPER** oder **XLOPER12** Werten sein. 
  
## <a name="return-value"></a>R�ckgabewert

Gibt die folgenden Werte für ganze Zahl (**Int**).
  
|**Wert**|**Rückgabecode**|**Beschreibung**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |Die Funktion wurde erfolgreich aufgerufen. Dies bedeutet, dass die Funktion einen Fehlerwert Excel nicht beendet wurde. um das herauszufinden, müssen Sie den Typ und den Wert des Parameters _PxRes_ resultierenden betrachten.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Der Befehl oder Funktion wurde fehlerbedingt beendet (interner Abbruch). Dies kann vorkommen eine XLM-Makrovorlage selbst geschlossen wird durch Aufrufen von **Schließen**oder Excel nicht genügend Arbeitsspeicher ist. Wenn Excel dieser Fehler zurückgibt, muss die aufrufende Funktion sofort beenden. Die DLL kann nur vor dem Beenden **XlFree** aufrufen. Alle anderen Aufrufe der C-API sind nicht zulässig. Der Benutzer kann keine Arbeit interaktiv speichern, mit dem Befehl **Speichern** im Menü **Datei** .  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Es wurde eine ungültige Funktionsnummer angegeben. Wenn Sie von der Headerdatei Xlcall.h Konstanten verwenden, sollte dies nicht der Fall, wenn Sie etwas aufrufen, die in der Version von Excel nicht unterstützt wird, das Sie ausführen.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Eine ungültige Anzahl von Argumenten eingegeben wurde. In Versionen bis zu Excel 2003 ist die maximale Anzahl von Argumenten, mit denen jede Funktion 30. Ab Excel 2007 ist die maximale Anzahl 255. Einige erfordern einer festen oder minimalen Anzahl von Argumenten.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Eine unzulässige **XLOPER** oder **XLOPER12** an die Funktion übergeben wurde, oder ein Argument vom falschen Typ verwendet wurde.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Stapelüberlauf. Verwenden Sie **XlStack** , um die Größe des Raums links auf den Stapel überwachen. Vermeiden Sie sehr große lokale (automatische) Arrays und Strukturen auf dem Stapel zuordnen, sofern möglich; Stellen sie statische. (Beachten Sie, dass ein Stapelüberlauf auftreten kann, ohne dass.)  <br/> |
|32  <br/> |**xlretFailed zurück** <br/> |Eine Funktion Befehl äquivalent ist fehlgeschlagen. Dies ist gleichbedeutend mit einer Makrobefehl das Dialogfeld Makro Fehler Warnung angezeigt.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Es wurde versucht, auf eine Zelle, die noch nicht berechnet Dereferenzierung, da es geplant ist, nach der aktuellen Zelle berechnet werden soll. In diesem Fall muss die DLL Steuerelement nach Excel sofort zurückgeben. Die DLL kann nur vor dem Beenden **XlFree** aufrufen. Alle anderen Aufrufe der C-API sind nicht zulässig. Weitere Informationen zu den Funktionen können und die Werte von Zellen, die nicht neu berechnet wurde, finden Sie unter [Excel-Befehle, Funktionen und-Zustände](excel-commands-functions-and-states.md)können nicht zugegriffen werden.  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Es wurde versucht, eine Funktion aufgerufen, die nicht oder möglicherweise nicht, während eine Multithread-neuberechnung der Arbeitsmappe threadsicheren.  <br/> Ab Excel 2007 dieser Wert wird zurückgegeben, und nur innerhalb der XLL Arbeitsblattfunktionen deklariert thread als Safe.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |Das Handle asynchronen Funktion ist ungültig.  <br/> Dieser Wert wird nur von Excel 2010 verwendet.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |Der Anruf wird auf Clustern nicht unterstützt.  <br/> Dieser Wert wird nur von Excel 2010 verwendet.  <br/> |
   
## <a name="remarks"></a>Hinweise

### <a name="valid-ifunction-values"></a>Gültige iFunction Werte

Gültige **iFunction** Werte sind in der Headerdatei Xlcall.h oder eine der folgenden speziellen Funktionen definiert Konstanten **Xlf...** oder **Xlc...** . 
  
|||||
|:-----|:-----|:-----|:-----|
|**Bereichsgröße** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**gleich xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Unterschiedliche Typen von Funktionen

 **Excel4** und **Excel12** unterscheiden, drei Klassen von Funktionen. Die Funktionen werden entsprechend der drei Zustände klassifiziert, in denen die DLL Excel aufgerufen werden kann. 
  
- Klasse 1 gilt, wenn die DLL aus einem Arbeitsblatt als Ergebnis einer neuberechnung aufgerufen wird. 
    
- Klasse 2 gilt, wenn die DLL aus aufgerufen wird, in einem Funktionsmakro oder aus einem Arbeitsblatt, in dem er mit einem Nummernzeichen (#) im Text Typ registriert wurde.
    
- Klasse 3 gilt, wenn ein Objekt, Makros, Menü, Symbolleiste, Tastenkombination, **ExecuteExcel4Macro** -Methode oder den Befehl **Tools/Makro/ausführen** eine DLL aufgerufen wird. Weitere Informationen finden Sie unter [Excel-Befehle, Funktionen und-Zustände](excel-commands-functions-and-states.md).
    
Die folgende Tabelle zeigt, welche Funktionen in jeder Klasse gültig sind.
  
|**1-Klasse**|**Klasse 2**|**Klasse 3**|
|:-----|:-----|:-----|
|Eine beliebige Arbeitsblattfunktion  <br/> Alle außer **gleich XlSet**XLL-only **... xl** -Funktion.  <br/> **xlfCaller** <br/> |Eine beliebige Arbeitsblattfunktion  <br/> Alle außer **gleich XlSet** **.. xl** -Funktion.  <br/> Makro Blatt Funktionen, einschließlich **XlfCaller**, die einen Wert zurück, verschiebt aber keine Aktion, die den Arbeitsbereich wirkt sich auf oder eine geöffnete Arbeitsmappe.  <br/> |Jede Funktion, einschließlich **gleich XlSet** und Funktionen, Befehl entspricht.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Anzeigen des Dialogfelds für einen Befehl Entsprechung-Funktion

Weist eine Funktion Befehl Entsprechung Dialogfeld zugeordnet ist, können Sie das **XlPrompt** Bit in **iFunction**festlegen. Dies bedeutet, dass Excel das entsprechende Dialogfeld vor der Ausführung des Befehls angezeigt.
  
### <a name="writing-international-dlls"></a>Schreiben von internationalen DLLs

Wenn Sie das **Xlintl32** Bit in **iFunction**festlegen, wird die Funktion oder den Befehl ausgeführt, als ob es aus einem Makroblatt International aufgerufen wurden. Dies bedeutet, dass der Befehl verhält sich, als würde die US-Version von Excel, auch wenn er auf eine internationale (lokalisierte) Version ausgeführt wird.
  
### <a name="xlretuncalced-or-xlretabort"></a>XlretUncalced oder xlretAbort

Nach dem Empfang einer der folgenden Werte zurückgeben, muss die DLL bereinigen und sofort die Steuerung an Excel zurück. Rückrufe in Excel über die C-API, mit Ausnahme von **XlFree**, sind deaktiviert, nach dem Empfang einer der folgenden Werte zurückgeben.
  
## <a name="example"></a>Beispiel

Im folgende Beispiel wird die **Excel12** -Funktion verwendet, auf um die Zelle zu markieren, von der sie aufgerufen wurde. 
  
Dieses Codebeispiel ist Teil eines umfangreicheren Beispiels in Excel 2010 XLL SDK am folgenden Speicherort, in dem Sie das SDK installiert:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Diese Funktion ruft ein Makro mit Befehlen (XlcSelect) und daher funktioniert nur, wenn sie von einer XLM-Makrovorlage aufgerufen wird. 
  
```cs
short WINAPI Excel12Example(void)
{
    XLOPER12 xRes;
    Excel12(xlfCaller, &xRes, 0);
    Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Excel4v/Excel12v](excel4v-excel12v.md)

