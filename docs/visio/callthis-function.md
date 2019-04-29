---
title: CALLTHIS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Ruft eine Prozedur in einem VBA-Projekt (Microsoft Visual Basic für Applikationen) auf.
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413815"
---
# <a name="callthis-function"></a>CALLTHIS Function

Ruft eine Prozedur in einem VBA-Projekt (Microsoft Visual Basic für Applikationen) auf.
  
## <a name="syntax"></a>Syntax

CALLTHIS ("* * *procedure* * *", ["* * *project* * *"], [* * *arg1* * *, * * *arg2* * *,...]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Prozedur_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name der Prozedur, die aufgerufen werden soll.  <br/> |
| _Projekt_ <br/> |Optional  <br/> |**String** <br/> |Das Projekt, das die Prozedur enthält.  <br/> |
| _arg_ <br/> |Optional  <br/> |**Number, String, Date oder Currency** <br/> |Wird als Parameter an die Prozedur übergeben,  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Im VBA-Projekt wird *Procedure* wie folgt definiert: 
  
Procedure (*vsoShape* as Visio. Shape [arg1 As Type, arg2 As Type...]) 
  
Dabei ist *vsoShape* ein Verweis auf das **Shape** -Objekt, das die CALLTHIS-Formel enthält, die ausgewertet wird, und _arg1_, *arg2* ... sind die in dieser Formel angegebenen Argumente. 
  
Beachten Sie, dass *vsoShape* dem Argument "This" ähnelt, das an eine C++-Member-Prozedur übergeben wird. Daher lautet der Name "CALLTHIS". Eine Zelle mit einer Formel, die CALLTHIS enthält, kann in der Tat wie folgt lauten: "diese Prozedur aufrufen und einen Verweis auf meine Form weitergeben." 
  
Wenn _Project_ angegeben ist, scannt Microsoft Visio alle geöffneten Dokumente für das Projekt und __ die Aufruf _Prozedur_ in diesem Projekt. Wenn _Project_ ausgelassen oder NULL ("") ist, wird von Visio die _Prozedur_ im VBA-Projekt des Dokuments, das die CALLTHIS-Formel enthält, die ausgewertet wird. 
  
Zahlen in _arg1_, _arg2..._ werden in externen Einheiten übergeben. Wenn Sie beispielsweise den Wert der Zelle Height aus einer Form übergeben, die 3 cm hoch ist, wird 3 übergeben. Wenn Sie verschiedene Einheiten mit einer Zahl übertragen möchten, verwenden Sie die FORMATEX-Funktion, oder erzwingen Sie explizit Einheiten, indem Sie ein NULL-Nummern Einheiten Paar (beispielsweise 0 Ft + Height) hinzufügen. 
  
Das zweite Komma in der CALLTHIS-Funktion ist optional. Es entspricht der Anzahl zusätzlicher Parameter, die der Prozedur hinzugefügt werden. Wenn Sie keine zusätzlichen Parameter verwenden, `(vsoShape as Visio.Shape)` dürfen Sie das zweite Komma nicht hinzufügen; Verwenden Sie CALLTHIS ("",). Wenn Sie beispielsweise zwei zusätzliche Parameter hinzufügen, verwenden Sie CALLTHIS("",,,). 
  
Die CALLTHIS-Funktion wertet immer 0 aus, und der Aufruf der _Prozedur_ tritt während der Leerlaufzeit nach Abschluss des neuberechnungs Prozesses auf.  _procedure_ kann einen Wert zurückgeben, der jedoch von Visio ignoriert wird.  _Prozedur_ gibt einen Wert zurück, der von Visio erkannt werden kann, indem die Formel oder das Ergebnis einer anderen Zelle im Dokument festgelegt wird, nicht jedoch die Zelle, die _Prozedur_aufgerufen wird, es sei denn, Sie möchten die CALLTHIS-Formel überschreiben.
  
Der Unterschied zwischen der CALLTHIS-Funktion und der RUNADDON-Funktion besteht darin, dass das Projekt eines Dokuments auf kein anderes Projekt verweisen muss, um Prozeduren in diesem Projekt aufrufen zu können. 
  
> [!NOTE]
>  VBA-Code, der aufgerufen wird, wenn die Visio-Instanz eine CALLTHIS-Funktion in einer Formel auswertet, darf das Dokument mit der Zelle, die die Funktion verwendet, nicht schließen, da dies zu einem Anwendungsfehler führt und Visio beendet wird. 
  
Wenn Sie das Dokument mit der Zelle, die die CALLTHIS-Funktion nutzt, schließen müssen, nutzen Sie eines der folgenden Verfahren: 
  
- Schließen Sie das Dokument mit Code, der kein VBA-Code ist.
    
- Schließen Sie das Dokument von einem anderen Projekt aus als von jenem, das gerade geschlossen wird.
    
- Fügen Sie Fenster-Nachrichten zum Schließen der Fenster ein, anstatt das Dokument zu schließen.
    
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
## <a name="example-1"></a>Beispiel 1

CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))
  
Ruft die in einem Modul abgelegte Prozedur namens p auf und übergibt den Wert der Zelle Height in Zentimetern, beispielsweise 7,62.
  
## <a name="example-2"></a>Beispiel 2

CALLTHIS("q",,0 cm+Height,Width)
  
Ruft die in einem Modul abgelegte Prozedur q auf und übergibt die Höhe der Zelle in Zentimetern und die Breite in internen Einheiten.
  
## <a name="example-3"></a>Beispiel 3

Verwenden Sie das folgende Verfahren im *ThisDocument* -Klassenmodul. 
  
Verwenden Sie mit den oben beschriebenen Prozeduren eines der folgenden Syntaxbeispiele in der Zelle EventDblClick eines Shapes.
  
CALLTHIS ("ThisDocument. A",)
  
CALLTHIS ("ThisDocument. B", "Click")
  
CALLTHIS("ThisDocument.C",,"Klicken Sie auf", "OK.")
  

