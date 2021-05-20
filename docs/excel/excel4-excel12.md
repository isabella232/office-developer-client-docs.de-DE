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
- excel4-Funktion [excel 2007],Excel12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 2404f10d-8641-4ee6-a909-1c5a26610f80
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7c3af5f380ae4144890b1f7b486a61a05c19de74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429446"
---
# <a name="excel4excel12"></a>Excel4/Excel12

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine interne Microsoft Excel, Makroblattfunktion oder -befehl oder XLL-only-Sonderfunktion oder -befehl innerhalb einer DLL/XLL- oder Coderessource auf.
  
Alle aktuellen Versionen von Excel **unterstützen Excel4**. Ab Excel 2007 wird **Excel12** unterstützt. 
  
Diese Funktionen können nur aufgerufen werden, Excel das Steuerelement an die DLL oder XLL übergeben hat. Sie können auch aufgerufen werden, wenn Excel die Steuerung indirekt über einen Aufruf von Visual Basic for Applications (VBA) übergeben hat. Sie können nicht zu einem anderen Zeitpunkt aufgerufen werden. Sie können z. B. nicht bei Aufrufen der [DllMain-Funktion](https://docs.microsoft.com/windows/desktop/dlls/dllmain) oder in anderen Zeiten aufgerufen werden, in denen das Betriebssystem die DLL aufgerufen hat, oder aus einem thread, der von der DLL erstellt wurde. 
  
Die [Funktionen Excel4v und Excel12v](excel4v-excel12v.md) akzeptieren ihre Argumente als Array, während die **Excel4-** und **Excel12-Funktionen** ihre Argumente als Liste mit variabler Länge auf dem Stapel akzeptieren. In allen anderen Hinsicht verhält sich **Excel4** genauso wie **Excel4v,** und **Excel12** verhält sich genauso wie **Excel12v**.
  
```cs
int Excel4(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER argument1, ...);
int Excel12(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**int**)
  
Eine Zahl, die den Befehl, die Funktion oder die Sonderfunktion angibt, die Sie aufrufen möchten. Eine Liste der  _gültigen iFunction-Werte_ finden Sie im folgenden Abschnitt "Hinweise". 
  
 _pxRes_ (**LPXLOPER** oder **LPXLOPER12**)
  
Ein Zeiger auf einen **XLOPER** (mit **Excel4**) oder einen **XLOPER12** (mit **Excel12),** der das Ergebnis der ausgewerteten Funktion hält.
  
 _iCount_ (**int**)
  
Die Anzahl der nachfolgenden Argumente, die an die Funktion übergeben werden. In Versionen von Excel bis 2003 kann dies eine beliebige Zahl zwischen 0 und 30 sein. Ab Excel 2007 kann dies eine beliebige Zahl zwischen 0 und 255 sein.
  
 _argument1, ..._ (**LPXLOPER** oder **LPXLOPER12**)
  
Die optionalen Argumente für die Funktion. Alle Argumente müssen Zeiger auf **XLOPER-** oder **XLOPER12-Werte** sein. 
  
## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden ganzzahligen Werte (**int**) zurück.
  
|**Wert**|**Rückgabecode**|**Beschreibung**|
|:-----|:-----|:-----|
|0  <br/> |**xlretSuccess** <br/> |Die Funktion wurde erfolgreich aufgerufen. Dies bedeutet nicht, dass die Funktion keinen Fehlerwert Excel hat. Um dies herauszufinden, müssen Sie sich den Typ und Wert des resultierenden _pxRes-Parameters_ anschauen.  <br/> |
|1  <br/> |**xlretAbort** <br/> |Der Befehl oder die Funktion wurde anormal beendet (interner Abbruch). Dies kann auftreten, wenn sich ein XLM-Makroblatt durch Aufrufen von **CLOSE** schließt oder Excel nicht genügend Arbeitsspeicher hat. Wenn Excel diesen Fehler zurückgibt, muss die aufrufende Funktion sofort beendet werden. Die DLL darf **xlFree** nur vor dem Beenden aufrufen. Alle anderen Aufrufe der C-API sind nicht zulässig. Der Benutzer kann alle Arbeiten interaktiv speichern, indem er den **Befehl Speichern** im Menü **Datei** verwendet.  <br/> |
|2  <br/> |**xlretInvXlfn** <br/> |Eine ungültige Funktionsnummer wurde angegeben. Wenn Sie Konstanten aus der Xlcall.h-Headerdatei verwenden, sollte dies nur auftreten, wenn Sie etwas aufrufen, das in der Version von Excel nicht unterstützt wird.  <br/> |
|4   <br/> |**xlretInvCount** <br/> |Es wurde eine ungültige Anzahl von Argumenten eingegeben. In Versionen bis Excel 2003 beträgt die maximale Anzahl von Argumenten, die eine Funktion verwenden kann, 30. Ab Excel 2007 beträgt die maximale Anzahl 255. Einige erfordern eine feste oder minimale Anzahl von Argumenten.  <br/> |
|8   <br/> |**xlretInvXloper** <br/> |Ein **ungültiger XLOPER-** oder **XLOPER12-Wert** wurde an die Funktion übergeben, oder es wurde ein Argument des falschen Typs verwendet.  <br/> |
|16   <br/> |**xlretStackOvfl** <br/> |Ein Stapelüberlauf ist aufgetreten. Verwenden **Sie xlStack,** um die Menge des auf dem Stapel noch vorhandenen Platzes zu überwachen. Vermeiden Sie, möglichst große lokale (automatische) Arrays und Strukturen auf dem Stapel zuzuordnen. sie statisch machen. (Beachten Sie, dass ein Stapelüberlauf auftreten kann, ohne erkannt zu werden.)  <br/> |
|32  <br/> |**xlretFailed** <br/> |Fehler bei einer befehlsäquivalenten Funktion. Dies entspricht einem Makrobefehl, in dem das Dialogfeld Makrofehlerwarnung angezeigt wird.  <br/> |
|64  <br/> |**xlretUncalced** <br/> |Es wurde versucht, eine Noch nicht berechnete Zelle zu dereferenzieren, da sie nach der aktuellen Zelle neu berechnet werden soll. In diesem Fall sollte die DLL das Steuerelement sofort Excel zurückgeben. Die DLL darf **xlFree** nur vor dem Beenden aufrufen. Alle anderen Aufrufe der C-API sind nicht zulässig. Weitere Informationen dazu, welche Funktionen auf die Werte von Zellen zugreifen können und nicht, die nicht neu berechnet wurden, finden Sie unter [Excel Commands, Functions, and States](excel-commands-functions-and-states.md).  <br/> |
|128  <br/> |**xlretNotThreadSafe** <br/> |Es wurde versucht, eine Funktion aufrufen, die bei einer Mehrthreadneuberechnung der Arbeitsmappe nicht threadsicher oder möglicherweise nicht threadsicher ist.  <br/> Ab Excel 2007 wird dieser Wert zurückgegeben, und nur innerhalb von Als threadsicher deklarierten XLL-Arbeitsblattfunktionen.  <br/> |
|256  <br/> |**xlRetInvAsynchronousContext** <br/> |Das asynchrone Funktionshandle ist ungültig.  <br/> Dieser Wert wird nur von 2010 Excel verwendet.  <br/> |
|512  <br/> |**xlRetNotClusterSafe** <br/> |Der Aufruf wird in Clustern nicht unterstützt.  <br/> Dieser Wert wird nur von 2010 Excel verwendet.  <br/> |
   
## <a name="remarks"></a>Hinweise

### <a name="valid-ifunction-values"></a>Gültige iFunction-Werte

Gültige **iFunction-Werte** sind alle **xlf...-** oder **xlc...-Konstanten,** die in der Xlcall.h-Headerdatei oder einer der folgenden Speziellen Funktionen definiert sind. 
  
|||||
|:-----|:-----|:-----|:-----|
|**xlAbort** <br/> |**xlEnableXLMsgs** <br/> |**xlGetInst** <br/> |**xlSheetNm** <br/> |
|**xlCoerce** <br/> |**xlFree** <br/> |**xlGetName** <br/> |**xlStack** <br/> |
|**xlDefineBinaryName** <br/> |**xlGetBinaryName** <br/> |**xlSet** <br/> |**xlUDF** <br/> |
|**xlDisableXLMsgs** <br/> |**xlGetHwnd** <br/> |**xlSheetId** <br/> ||
   
### <a name="different-types-of-functions"></a>Verschiedene Arten von Funktionen

 **Excel4** und **Excel12** unterscheiden zwischen drei Klassen von Funktionen. Die Funktionen werden nach den drei Zuzuständen klassifiziert, in denen Excel DLL aufrufen können. 
  
- Klasse 1 gilt, wenn die DLL aus einem Arbeitsblatt als Ergebnis einer Neuberechnung aufgerufen wird. 
    
- Klasse 2 gilt, wenn die DLL innerhalb eines Funktionsmakros oder aus einem Arbeitsblatt aufgerufen wird, in dem sie mit einem Nummernzeichen (#) im Typtext registriert wurde.
    
- Klasse 3 gilt, wenn eine DLL von einem Objekt, Makro, Menü, Symbolleiste, Tastenkombination, **ExecuteExcel4Macro-Methode** oder dem **Befehl Extras/Makro/Ausführen** aufgerufen wird. Weitere Informationen finden Sie [unter Excel Befehle, Funktionen und Zustände](excel-commands-functions-and-states.md).
    
Die folgende Tabelle zeigt, welche Funktionen in den einzelnen Klassen gültig sind.
  
|**Klasse 1**|**Klasse 2**|**Klasse 3**|
|:-----|:-----|:-----|
|Beliebige Arbeitsblattfunktion  <br/> Alle XLL-only **xl...-Funktionen** außer **xlSet**.  <br/> **xlfCaller** <br/> |Beliebige Arbeitsblattfunktion  <br/> Alle **xl...-Funktionen** außer **xlSet**.  <br/> Makroblattfunktionen, einschließlich **xlfCaller**, die einen Wert zurückgeben, aber keine Aktion ausführen, die sich auf den Arbeitsbereich oder eine geöffnete Arbeitsmappe auswirkt.  <br/> |Jede Funktion, einschließlich **xlSet-** und befehlsäquivalenter Funktionen.  <br/> |
   
### <a name="displaying-the-dialog-box-for-a-command-equivalent-function"></a>Anzeigen des Dialogfelds für eine Command-Equivalent Funktion

Wenn einer befehlsäquivalenten Funktion ein Dialogfeld zugeordnet ist, können Sie das **xlPrompt-Bit** in **iFunction festlegen.** Dies bedeutet, Excel das entsprechende Dialogfeld vor dem Ausführen des Befehls anzeigt.
  
### <a name="writing-international-dlls"></a>Schreiben von internationalen DLLs

Wenn Sie das **xlIntl-Bit** in **iFunction** festlegen, wird die Funktion oder der Befehl so ausgeführt, als ob es von einem internationalen Makroblatt aufgerufen würde. Dies bedeutet, dass sich der Befehl wie in der US-Version von Excel verhält, auch wenn er auf einer internationalen (lokalisierten) Version ausgeführt wird.
  
### <a name="xlretuncalced-or-xlretabort"></a>xlretUncalced oder xlretAbort

Nachdem Sie einen dieser Rückgabewerte erhalten haben, muss Ihre DLL die Steuerung sofort bereinigen und Excel zurückgeben. Rückrufe in Excel über die C-API mit Ausnahme von **xlFree** werden deaktiviert, nachdem sie einen dieser Rückgabewerte erhalten haben.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird die **Excel12-Funktion** verwendet, um die Zelle auszuwählen, aus der sie aufgerufen wurde. 
  
Dieses Codebeispiel ist Teil eines größeren Beispiels, das im Excel 2010 XLL SDK am folgenden Speicherort bereitgestellt wird, an dem Sie das SDK installiert haben:
  
\Samples\Example\Example.c.
  
> [!NOTE]
> Diese Funktion ruft ein Befehlsmakro (xlcSelect) auf und funktioniert daher nur, wenn es von einem XLM-Makroblatt aufgerufen wird. 
  
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

