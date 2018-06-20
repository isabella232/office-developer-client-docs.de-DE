---
title: Zugriff auf XLL-Code in Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- Zugriff auf Xll-Code [excel 2007], XLLs [Excel 2007], den Zugriff auf Code, Befehle [Excel 2007], Registrierung, Funktionen [Excel 2007], Registrierung, Aufrufen von XLLs in Excel, Befehle [Excel 2007] registrieren, registrieren Funktionen [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790391"
---
# <a name="accessing-xll-code-in-excel"></a>Zugriff auf XLL-Code in Excel

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
In Microsoft Excel, Funktionen und Befehle, die eine XLL enthält verfügbar sein:
  
- Muss von der XLL exportiert werden.
    
- Muss mit Excel registriert werden.
    
## <a name="registering-functions-and-commands-with-excel"></a>Registrieren von Funktionen und Befehle mit Excel

Registrierung teilt Excel die folgenden Informationen zu einer DLL-Einstiegspunkt:
  
- Ob er ausgeblendet wurde oder wenn eine Funktion, wird es gibt an, ob in den Funktions-Assistenten angezeigt.
    
- Gibt an, ob es aufrufbare nur aus einer XLM-Makrovorlage oder aus einem Arbeitsblatt ist.
    
- Wenn ein Befehl, ob ist es einer Tabellenfunktion oder einer gleichwertigen Blatt Makrofunktion.
    
- Welchen XLL-DLL Exportnamen hat, und welche Namen Excel verwendet werden soll.
    
- Wenn es sich um eine Funktion ist:
    
  - Welche Daten gibt es gibt und als Argumente.
    
  - Gibt an, ob sie das Ergebnis zurückgegeben, indem ein Argument direkten ändern.
    
  - Gibt an, ob es veränderliche ist.
    
  - Gibt an, ob es threadsicheren (unterstützte beginnend in Excel 2007) ist.
    
  - Was Text einfügen Funktions-Assistenten und AutoVervollständigen-Editor angezeigt werden soll, das Ihnen bei Aufruf der Funktion.
    
  - Die Funktion Kategorie, die unter aufgelistet werden soll.
    
Dies geschieht alle mit der C-API-Funktion [XlfRegister](xlfregister-form-1.md), entspricht die XLM-Funktion **zu registrieren**.
  
## <a name="calling-xll-functions-directly-from-excel"></a>Aufrufen von XLL-Funktionen direkt in Excel

Nachdem sie registriert sind, können XLL Arbeitsblatt und Makro Blatt Funktionen unabhängig vom Standort aufgerufen werden, die, denen eine integrierte Funktion aus aufgerufen werden kann:
  
- Eine einzelne Zelle oder ein Array der Formel in einem Arbeitsblatt.
    
- Eine einzelne Zelle oder ein Array der Formel in einem Makroblatt.
    
- Die Definition eines definierten Namens.
    
- Die Bedingung und höhere Felder in einem Dialogfeld Bedingte Formatierung.
    
- Aus einer anderen-add-in über die C-API-Funktion [XlUDF](xludf.md).
    
- In Visual Basic für Applikationen (VBA) über die **entsprechende** Methode. 
    
Sie können einen Verweis auf die aufrufende Zelle oder eines Zellbereichs innerhalb Ihrer Funktion mit der C-API-Funktion **XlfCaller**abzurufen. Wenn die Funktion die Zelle bedingtes Format Ausdruck aufgerufen wurde, werden Sie dennoch einen Verweis auf die zugeordnete Zelle oder Zellen, zurückgegeben, sodass Sie können nicht davon ausgehen, dass die Formel der Zelle XLL-Funktion enthält. Wenn Ihre Funktion aus einer VBA-benutzerdefinierte Funktion (UDF) aufgerufen wurde, gibt **XlfCaller** erneut die Adresse der Zellen, die die VBA-Funktion aufgerufen. Weitere Informationen finden Sie unter [XlfCaller](xlfcaller.md).
  
> [!NOTE]
> Excel ruft auch XLL-Funktionscode die Dialogfelder **Einfügen Funktions-Assistenten** , und **Ersetzen** . Sie müssen möglicherweise Ihr Codes normal ausgeführt, in die Groß-/Kleinschreibung im Dialogfeld **Funktionsargumente einfügen** , insbesondere, in dem Ihre Funktion sehr lange führen Sie ergreifen kann, einschränken. Zum Erkennen von einer der folgenden Dialogfelder Ihre Funktion aufgerufen wird, muss Implementierung Teil des Codes in Ihrem Projekt, die durchlaufen und alle geöffneten Fenster zu ermitteln, ob das Front-Fenster ist eines der folgenden Dialogfelder, und wenn Ja, welche. 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Aufrufen von XLL-Befehle direkt in Excel

Nachdem sie registriert sind, können XLL-Befehle in allen Verfahren aufgerufen werden, dass andere benutzerdefinierte Makros aufgerufen werden können:
  
- Durch ein Control-Objekt zugeordnet wird, die in einem Arbeitsblatt eingebettet werden.
    
- Im Dialogfeld Makro ausführen.
    
- In VBA-Makro verwenden Sie die **entsprechende** Methode. 
    
- Über ein benutzerdefiniertes Menüelement oder eine Symbolleiste.
    
- Mithilfe einer Tastenkombination eingerichtet werden, wenn Sie den Befehl registriert.
    
- Wie der Befehl ausgeführt werden soll, wenn ein bestimmtes Ereignis aufgefangen.
    
> [!NOTE]
> XLL-Befehle werden ausgeblendet, dass sie nicht in der Liste der verfügbaren Makros in Excel-Dialogfelder angezeigt. Jedoch manuell in das Feld Makro ein eingegeben werden. Excel erwartet, dass der Name registriert als in diesen Dialogfeldern nicht der Name der DLL-Datei exportieren. 
  
Alle XLL-Befehle mit Excel registriert werden angenommen, dass von Excel im folgenden Format sein:
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

[!HINWEIS] Der R�ckgabewert wird von Excel ignoriert, es sei denn, der Aufruf erfolgt aus einer XLM-Makrovorlage; in diesem Fall wird der R�ckgabewert in **TRUE** oder **FALSE** konvertiert. Sie m�ssen daher 1 zur�ckgeben, wenn der Befehl erfolgreich ausgef�hrt wurde, und 0 bei einem Fehler oder Benutzerabbruch.
  
Erhalten Sie Informationen zu den gewünschten Befehl wie aufgerufen wurde mit der C-API-Funktion **XlfCaller**. Weitere Informationen finden Sie unter [XlfCaller](xlfcaller.md).
  
Starten in Excel 2007-Benutzeroberfläche ist sehr unterschiedliche aus früheren Versionen. In den meisten Fällen werden weiterhin die C-API-Funktionen, die das Hinzufügen und Löschen von benutzerdefinierten Menüleisten, Menüs, Untermenüs, Menüelemente, benutzerdefinierte Symbolleisten und Symbolleistenschaltflächen ermöglichen unterstützt. Jedoch können sie nicht immer das hinzugefügte Element in eine Möglichkeit zur Verfügung, denen Ihre Benutzer mit vertraut sind. Sie sollten sorgfältig überprüfen, dass zusätzliche Funktionen weiterhin verfügbar ist, oder implementieren eine versionsspezifischen Anpassung. Starten von der Benutzeroberfläche in Excel 2007 ist am besten angepasst, mithilfe eines Moduls von verwaltetem Code, das dann eng mit Ihrer XLL-Befehle verknüpft werden kann.
  
## <a name="see-also"></a>Siehe auch

- [Erstellen von XLLs](creating-xlls.md)
- [Anruf XLL-Funktionen aus der Funktions-Assistenten oder Dialogfelder ersetzen](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)
- [Entwickeln von Excel-XLLs](developing-excel-xlls.md)



