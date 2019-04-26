---
title: Zugreifen auf XLL-Code in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugreifen auf XLL-Code [Excel 2007],XLLs [Excel 2007], Zugreifen auf Code, Befehle [Excel 2007], Registrierung, Funktionen [Excel 2007], Registrierung, Aufrufen von XLLs aus Excel, Registrieren von Befehlen [Excel 2007], Registrieren von Funktionen [Excel 2007]
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d1332b0dffc052404c75c4ec51d94879457c3da0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304186"
---
# <a name="accessing-xll-code-in-excel"></a>Zugreifen auf XLL-Code in Excel

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Um in Microsoft Excel zur Verfügung zu stehen, müssen die Funktionen und Befehle, die eine XLL enthält:
  
- von der XLL exportiert werden.
    
- bei Excel registriert werden.
    
## <a name="registering-functions-and-commands-with-excel"></a>Registrieren von Funktionen und Befehlen bei Excel

Die Registrierung informiert Excel über Folgendes hinsichtlich eines DLL-Einstiegspunkts:
  
- Ob er ausgeblendet oder, wenn es sich um eine Funktion handelt, ob er im Funktionsassistenten sichtbar ist.
    
- Ob er nur aus einer XLM-Makrovorlage oder auch aus einem Arbeitsblatt aufrufbar ist.
    
- Wenn es sich um einen Befehl handelt, ob er eine Arbeitsblattfunktion oder eine äquivalente Makrovorlagenfunktion ist.
    
- Wie der XLL/DLL-Exportname lautet und welchen Namen Excel verwenden soll.
    
- Wenn es sich um eine Funktion handelt:
    
  - Welche Datentypen er als Argumente zurückgibt und erhält.
    
  - Ob er sein Ergebnis zurückgibt, indem er ein vorhandenes Argument ändert.
    
  - Ob er veränderbar ist.
    
  - Ob er Thread-sicher ist (unterstützt ab Excel 2007).
    
  - Welchen Text der Assistent zum Einfügen von Funktionen und der AutoVervollständigen-Editor anzeigen sollen, um beim Funktionsabruf zu unterstützen.
    
  - Unter welcher Funktionskategorie er aufgelistet werden soll.
    
Dies wird alles mit der C-API-Funktion [xlfRegister](xlfregister-form-1.md) erreicht, die der XLM-Funktion **REGISTER** entspricht.
  
## <a name="calling-xll-functions-directly-from-excel"></a>Aufrufen von XLL-Funktionen direkt aus Excel

Sobald sie registriert sind, können die Funktionen von XLL-Arbeitsblatt und Makrovorlage dort aufgerufen werden, wo eine integrierte Funktion aufgerufen werden kann:
  
- Einzelzellen- oder Array-Formel in einem Arbeitsblatt.
    
- Einzelzellen- oder Array-Formel in einer Makrovorlage.
    
- Definition eines definierten Namens.
    
- Bedingungs- und Grenzwertfelder in einem Bedingungsformat-Dialogfeld.
    
- Anderes Add-In über die C-API-Funktion [xlUDF](xludf.md).
    
- Aus Visual Basic for Applications (VBA) über die **Application.Run**-Methode. 
    
Sie erhalten eine Referenz zur aufrufenden Zelle oder zum aufrufenden Zellenbereich in der Funktion mit der C-API-Funktion **xlfCaller**. Wenn die Funktion aus dem Bedingungsformatausdruck der Zelle aufgerufen wurde, erhalten Sie weiterhin eine Referenz zu den verknüpften Zellen. Das heißt, Sie können nicht davon ausgehen, dass die Zellenformel die XLL-Funktion enthält. Wenn Ihre Funktion aus einer benutzerdefinierten VBA-Funktion (UDF) aufgerufen wurde, gibt **xlfCaller** erneut die Adresse der Zellen zurück, die die VBA-Funktion aufgerufen haben. Weitere Informationen finden Sie unter [xlfCaller](xlfcaller.md).
  
> [!NOTE]
> Excel ruft auch XLL-Funktionscode aus den Dialogfelder **Funktionsassistent einfügen** und **Ersetzen** auf. Sie müssen evtl. die normale Ausführung Ihres Codes im Dialogfeld **Funktionsargumente einfügen** einschränken, insbesondere wenn Ihre Funktion nur langsam ausgeführt wird. Um zu erkennen, ob Ihre Funktion aus einem dieser Dialogfelder aufgerufen wird, müssen Sie Code in Ihrem Projekt implementieren, der durch alle geöffneten Fenster iteriert, um zu ermitteln, ob das Fenster im Vordergrund eines dieser Dialogfelder ist, und, wenn ja, welches. 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Direktes Aufrufen von XLL-Befehlen aus Excel

Sobald sie registriert sind, können XLL-Befehle so wie andere benutzerdefinierte Makros aufgerufen werden:
  
- Durch Zuordnung zu einem Steuerungsobjekt in einem Arbeitsblatt.
    
- Im Dialogfeld „Makro ausführen“.
    
- Aus einem benutzerdefinierten VBA-Makro mit der **Application.Run**-Methode. 
    
- Aus einem angepassten Menüelement oder einer angepassten Symbolleiste.
    
- Mithilfe einer Tastenkombination, die beim Registrieren des Befehls eingerichtet wurde.
    
- Als Befehl, der beim Abfangen eines bestimmten Ereignisses ausgeführt wird.
    
> [!NOTE]
> XLL-Befehle sind ausgeblendet. Sie werden nicht in der Liste der verfügbaren Makros in Excel-Dialogfeldern angezeigt. Aber sie können manuell in das Feld „Makroname“ eingegeben werden. Excel erwartet den Registriert als-Namen in diesen Dialogfeldern, nicht den DLL-Exportnamen. 
  
Für alle bei Excel registrierten XLL-Befehle wird von Excel die folgende Form vorausgesetzt:
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

Der Rückgabewert wird von Excel ignoriert, es sei denn, der Aufruf erfolgt aus einer XLM-Makrovorlage; in diesem Fall wird der Rückgabewert in **TRUE** oder **FALSE** konvertiert. Sie müssen daher 1 zurückgeben, wenn der Befehl erfolgreich ausgeführt wurde, und 0 bei einem Fehler oder Benutzerabbruch.
  
Sie erhalten mit der C-API-Funktion **xlfCaller** Informationen darüber, wie Ihr Befehl abgerufen wurde. Weitere Informationen finden Sie unter [xlfCaller](xlfcaller.md).
  
Ab Excel 2007 unterscheidet sich die Benutzeroberfläche deutlich von früheren Versionen. Die C-API-Funktionen, die das Hinzufügen und Löschen von benutzerdefinierten Menüleisten, Menüs, Untermenüs, Menüelementen, benutzerdefinierten Symbolleisten und Symbolleistenschaltflächen zulassen, werden weiterhin in den meisten Fällen unterstützt. Jedoch stellen sie evtl. nicht immer das hinzugefügte Element in einer Weise bereit, die Benutzern vertraut ist. Sie sollten sorgfältig prüfen, dass jegliche hinzugefügte Funktionalität weiterhin zugänglich ist, oder eine versionsspezifische Anpassung implementieren. Beim Starten in Excel 2007 wird die Benutzeroberfläche am besten über ein verwaltetes Codemodul angepasst, das eng mit Ihren XLL-Befehlen gekoppelt werden kann.
  
## <a name="see-also"></a>Siehe auch

- [Erstellen von XLLs](creating-xlls.md)
- [Aufrufen von XLL-Funktionen aus dem Funktionsassistenten oder Ersetzen von Dialogfeldern](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [Add-In-Manager und XLL-Schnittstellenfunktionen](add-in-manager-and-xll-interface-functions.md)
- [Entwickeln von XLLs für Excel](developing-excel-xlls.md)



