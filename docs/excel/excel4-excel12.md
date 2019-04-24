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
- Excel4-Funktion [Excel 2007], Excel12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304109"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine interne Microsoft Excel-Arbeitsblattfunktion, eine Makroblatt Funktion oder einen Befehl oder eine XLL-spezifische Funktion oder einen Befehl aus einer DLL/XLL-oder Coderessource auf.
  
Alle neueren Versionen von Excel unterstützen **Excel4**. Ab Excel 2007 wird **Excel12** unterstützt. 
  
Diese Funktionen können nur aufgerufen werden, wenn Excel die Steuerung an die DLL oder XLL übergeben hat. Sie können auch aufgerufen werden, wenn Excel die Steuerung indirekt über einen Aufruf von Visual Basic für Applikationen (VBA) übergeben hat. Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden. Beispielsweise können Sie nicht während der Aufrufe an die [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) -Funktion oder zu anderen Zeiten aufgerufen werden, wenn das Betriebssystem die dll aufgerufen hat, oder aus einem von der dll erstellten Thread. 
  
Die [Excel4v-und Excel12v-](excel4v-excel12v.md) Funktionen akzeptieren ihre Argumente als Array, wohingegen die **Excel4** -und die **Excel12** -Funktion Ihre Argumente als Liste mit variabler Länge im Stapel akzeptieren. In allen anderen Aspekten verhält sich **Excel4** wie **Excel4v**, und **Excel12** verhält sich genauso wie **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**int**)
  
Eine Zahl, die den Befehl, die Funktion oder die spezielle Funktion angibt, die Sie aufrufen möchten. Eine Liste gültiger _iFunction_ -Werte finden Sie im folgenden Abschnitt. 
  
 _pxRes_ (**LPXLOPER** oder **LPXLOPER12**)
  
Ein Zeiger auf ein **XLOPER** (mit **Excel4**) oder ein **XLOPER12** (mit **Excel12**), das das Ergebnis der ausgewerteten Funktion enthält.
  
 _iCount_ (**int**)
  
Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden. In Excel-Versionen bis zu 2003 kann es sich um eine beliebige Zahl zwischen 0 und 30 handeln. Ab Excel 2007 kann es sich um eine beliebige Zahl zwischen 0 und 255 handeln.
  
 _Argument1,._ .. (**LPXLOPER** oder **LPXLOPER12**)
  
Die optionalen Argumente für die Funktion. Alle Argumente müssen Zeiger auf **XLOPER** -oder **XLOPER12** -Werte sein. 
  
## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Integer-Werte (**int**) zurück.
  
|**Wert**|**Rückgabecode**|**Beschreibung**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |Die Funktion wurde erfolgreich aufgerufen. Dies bedeutet nicht, dass die Funktion keinen Excel-Fehlerwert zurückgegeben hat; um dies herauszufinden, müssen Sie den Typ und den Wert des resultierenden _pxRes_ -Parameters betrachten.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Der Befehl oder die Funktion wurde abnormal abgebrochen (interner Abbruch). Dies kann vorkommen, wenn eine XML-Makrovorlage sich selbst schließt, indem **Close**aufgerufen wird oder wenn Excel nicht genügend Arbeitsspeicher aufweist. Wenn Excel diesen Fehler zurückgibt, muss die aufrufende Funktion sofort beendet werden. Die DLL darf **xlFree** nur aufrufen, bevor Sie beendet wird. Alle anderen Aufrufe der C-API sind nicht zulässig. Der Benutzer kann alle arbeiten interaktiv speichern, indem er im Menü **Datei** den Befehl **Speichern** verwendet.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Es wurde eine ungültige Funktionsnummer angegeben. Wenn Sie Konstanten aus der Headerdatei xlcall. h verwenden, sollte dies nicht geschehen, es sei denn, Sie rufen etwas auf, das in der von Ihnen verwendeten Version von Excel nicht unterstützt wird.  <br/> |
|4  <br/> |**xlretInvCount** <br/> |Es wurde eine ungültige Anzahl von Argumenten eingegeben. In Versionen bis Excel 2003 ist die maximale Anzahl von Argumenten, die eine Funktion annehmen kann, 30. Ab Excel 2007 ist die maximale Anzahl 255. Einige erfordern eine feste oder minimale Anzahl von Argumenten.  <br/> |
|8  <br/> |**xlretInvXloper** <br/> |Ein ungültiger **XLOPER** oder **XLOPER12** wurde an die Funktion übergeben, oder es wurde ein Argument des falschen Typs verwendet.  <br/> |
|16  <br/> |**xlretStackOvfl** <br/> |Ein Stapelüberlauf ist aufgetreten. Verwenden Sie **xlStack** zum Überwachen des Speicherplatzes auf dem Stapel. Vermeiden Sie, dass sehr große lokale (automatische) Arrays und Strukturen, soweit möglich, auf dem Stapel reserviert werden. machen Sie Sie statisch. (Beachten Sie, dass ein Stapelüberlauf auftreten kann, ohne erkannt zu werden.)  <br/> |
|32  <br/> |**xlretFailed** <br/> |Fehler bei einer Befehls äquivalenten Funktion. Dies entspricht einem Makrobefehl, der das Dialogfeld Makro Fehler Warnung anzeigt.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Es wurde versucht, eine Zelle zu dereferenzieren, die noch nicht berechnet wurde, da Sie nach der aktuellen Zelle neu berechnet werden soll. In diesem Fall sollte die DLL die Steuerung sofort an Excel zurückgeben. Die DLL darf **xlFree** nur aufrufen, bevor Sie beendet wird. Alle anderen Aufrufe der C-API sind nicht zulässig. Weitere Informationen dazu, welche Funktionen auf die Werte von Zellen zugreifen können, die nicht neu berechnet wurden, finden Sie unter [Excel-Befehle,-Funktionen und-Zustände](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Es wurde versucht, eine Funktion aufzurufen, die während einer Multithread-Neuberechnung der Arbeitsmappe nicht oder nicht threadsicher ist.  <br/> Ab Excel 2007 wird dieser Wert zurückgegeben, und zwar nur innerhalb der XLL-Arbeitsblattfunktionen, die als threadsicher deklariert werden.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |Der asynchrone Funktions Handle ist ungültig.  <br/> Dieser Wert wird nur von Excel 2010 verwendet.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |Der Aufruf wird auf Clustern nicht unterstützt.  <br/> Dieser Wert wird nur von Excel 2010 verwendet.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

### <a name="valid-ifunction-values"></a>Gültige iFunction-Werte

Gültige **iFunction** -Werte sind beliebige der **XLF...** oder **XLC.** ..-Konstanten, die in der Headerdatei xlcall. h oder einer der folgenden speziellen Funktionen definiert sind. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Unterschiedliche Funktionstypen

 **Excel4** und **Excel12** unterscheiden zwischen drei Funktionsklassen. Die Funktionen werden gemäß den drei Status klassifiziert, in denen Excel die DLL aufrufen kann. 
  
- Klasse 1 gilt, wenn die DLL als Ergebnis einer Neuberechnung aus einem Arbeitsblatt aufgerufen wird. 
    
- Klasse 2 gilt, wenn die DLL aus einem Funktions Makro oder aus einem Arbeitsblatt aufgerufen wird, in dem Sie mit einem Nummernzeichen (#) im Typtext registriert wurde.
    
- Klasse 3 gilt, wenn eine DLL von einem Objekt, einem Makro, einem Menü, einer Symbolleiste, einer Tastenkombination, einer **ExecuteExcel4Macro** -Methode oder dem Befehl **Extras/Makro/ausführen** aufgerufen wird. Weitere Informationen finden Sie unter [Excel-Befehle,-Funktionen und-Zustände](excel-commands-functions-and-states.md).
    
In der folgenden Tabelle wird gezeigt, welche Funktionen in den einzelnen Klassen gültig sind.
  
|**Klasse 1**|**Klasse 2**|**Klasse 3**|
|:-----|:-----|:-----|
|Beliebige Arbeitsblattfunktion  <br/> Jede XLL-only **XL...** -Funktion außer **xlSet**.  <br/> **xlfCaller** <br/> |Beliebige Arbeitsblattfunktion  <br/> Jede **XL...** -Funktion außer **xlSet**.  <br/> Makroblatt Funktionen, einschließlich **xlfCaller**, die einen Wert zurückgeben, jedoch keine Aktion ausführen, die sich auf den Arbeitsbereich oder eine beliebige geöffnete Arbeitsmappe auswirkt.  <br/> |Eine beliebige Funktion, einschließlich **xlSet** -und Command-Equivalent-Funktionen.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Anzeigen des Dialog Felds für eine Befehlsäquivalente Funktion

Wenn eine Befehlsäquivalente Funktion über ein zugehöriges Dialogfeld verfügt, können Sie das **xlPrompt** -Bit in **iFunction**festlegen. Dies führt dazu, dass Excel vor dem Ausführen des Befehls das entsprechende Dialogfeld anzeigt.
  
### <a name="writing-international-dlls"></a>Schreiben von internationalen DLLs

Wenn Sie das **xlIntl** -Bit in **iFunction**festlegen, wird die Funktion oder der Befehl ausgeführt, als würde er von einer internationalen Makrovorlage aufgerufen werden. Dies bedeutet, dass der Befehl sich so verhält wie in der US-Version von Excel, auch wenn er auf einer internationalen (lokalisierten) Version läuft.
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced oder xlretAbort

Nachdem Sie einen dieser Rückgabewerte erhalten haben, muss die DLL die Steuerung sofort bereinigen und an Excel zurückgeben. Rückrufe in Excel über die C-API, mit Ausnahme von **xlFree**, sind deaktiviert, nachdem Sie einen dieser Rückgabewerte erhalten haben.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die **Excel12** -Funktion verwendet, um die Zelle auszuwählen, von der Sie aufgerufen wurde. 
  
Dieses Codebeispiel ist Teil eines umfangreicheren Beispiels, das im Excel 2010 XLL SDK bereitgestellt wird, an folgendem Speicherort, an dem Sie das SDK installiert haben:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Diese Funktion Ruft ein Befehlsmakro (xlcSelect) auf und funktioniert daher nur, wenn es von einem XML-Makroblatt aufgerufen wird. 
  
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

