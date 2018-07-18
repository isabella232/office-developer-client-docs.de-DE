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
description: Ruft eine Prozedur in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt.
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796563"
---
# <a name="callthis-function"></a>CALLTHIS Function

Ruft eine Prozedur in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt.
  
## <a name="syntax"></a>Syntax

CALLTHIS ("** *Verfahren* **", ["** *Project* **"], [** *arg1* **, ** *arg2* **,...]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Verfahren_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name der Prozedur, die aufgerufen werden soll.  <br/> |
| _Projekt_ <br/> |Optional  <br/> |**String** <br/> |Das Projekt, das die Prozedur enthält.  <br/> |
| _arg_ <br/> |Optional  <br/> |**Number, String, Date oder Currency** <br/> |Wird als Parameter an die Prozedur übergeben,  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In das VBA-Projekt ist *Procedure* wie folgt definiert: 
  
Prozedur (*VsoShape* als Visio.Shape [arg1 als Typ arg2 als Type...]) 
  
wobei *VsoShape* einen Verweis auf ist sind das **Shape** -Objekt, das das auszuwertende CALLTHIS-Formel enthält, und _arg1_, *arg2* ... die Argumente in dieser Formel angegeben. 
  
Beachten Sie, dass diese *VsoShape* sehr ähnlich wie das "this"-Argument in C++ Member-Prozedur übergeben wird. daher der Name "CALLTHIS". Wirksam, kann eine Zelle, die eine Formel enthält, die CALLTHIS gelesen werden, wie "Diese Prozedur aufrufen und sie einen Verweis auf Mein Shape übergeben." 
  
Wenn das _Projekt_ angegeben ist, durchsucht Microsoft Visio alle geöffneten Dokumente für die eine enthaltenden _Projekt-_ und Anrufe _Verfahren_ in diesem Projekt. _Projekt_ ist nicht angegeben oder null (""); Visio wird davon ausgegangen, _Prozedur_ befindet sich in das VBA-Projekt des Dokuments, die die CALLTHIS-Formel enthält, die ausgewertet wird. 
  
Zahlen in _arg1_, _arg2..._ werden in externen Einheiten übergeben. Wenn Sie den Wert der Zelle Height aus einem Shape übergeben, die 3 cm hoch ist, wird beispielsweise 3 übergeben. Um andere Einheiten mit einer Zahl zu übergeben, verwenden Sie die FORMATEX-Funktion oder Erstellen einer Einheiten explizit durch null Zahl-Einheit-Paar, z. B. 0Fuß + Höhe hinzufügen. 
  
Das zweite Komma in der CALLTHIS-Funktion ist optional. Es entspricht der Anzahl zusätzlicher Parameter an die Prozedur hinzugefügt. Wenn Sie zusätzliche Parameter nicht verwenden, mit Ausnahme der `(vsoShape as Visio.Shape)` , fügen Sie das zweite Komma; keine Verwenden Sie CALLTHIS("",). Wenn Sie zwei zusätzliche Parameter hinzufügen, verwenden Sie beispielsweise CALLTHIS("",,,). 
  
Die CALLTHIS-Funktion wird stets als 0 ausgewertet, und der Aufruf von _Procedure_ erfolgt in der Leerlaufzeit nach Abschluss des neuberechnung Vorgangs.  _Procedure_ kann einen Wert zurückgeben, jedoch Visio ignoriert wird.  _Prozedur_ gibt eines Werts, das durch Festlegen der Formel oder das Ergebnis einer anderen Zelle im Dokument Visio erkennen kann, jedoch nicht auf die Zelle, die _Prozedur_aufgerufen, es sei denn, Sie die CALLTHIS-Formel überschreiben möchten.
  
Der Unterschied zwischen der CALLTHIS-Funktion und der RUNADDON-Funktion besteht darin, dass das Projekt eines Dokuments auf kein anderes Projekt verweisen muss, um Prozeduren in diesem Projekt aufrufen zu können. 
  
> [!NOTE]
>  VBA-Code, der aufgerufen wird, wenn die Visio-Instanz eine CALLTHIS-Funktion in einer Formel auswertet, darf das Dokument mit der Zelle, die die Funktion verwendet, nicht schließen, da dies zu einem Anwendungsfehler führt und Visio beendet wird. 
  
Wenn Sie das Dokument mit der Zelle, die die CALLTHIS-Funktion nutzt, schließen müssen, nutzen Sie eines der folgenden Verfahren: 
  
- Schließen Sie das Dokument mit Code, der kein VBA-Code ist.
    
- Schließen Sie das Dokument von einem anderen Projekt aus als von jenen, das gerade geschlossen wird.
    
- Fügen Sie Fenster-Nachrichten zum Schließen der Fenster ein, anstatt das Dokument zu schließen.
    
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
## <a name="example-1"></a>Beispiel 1

CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))
  
Ruft die in einem Modul abgelegte Prozedur namens p auf und übergibt den Wert der Zelle Height in Zentimetern, beispielsweise 7,62.
  
## <a name="example-2"></a>Beispiel 2

CALLTHIS("q",,0 cm+Height,Width)
  
Ruft die in einem Modul abgelegte Prozedur q auf und übergibt die Höhe der Zelle in Zentimetern und die Breite in internen Einheiten.
  
## <a name="example-3"></a>Beispiel 3

Verwenden Sie das folgende Verfahren im Klassenmodul *ThisDocument* . 
  
Verwenden Sie mit den oben beschriebenen Prozeduren eines der folgenden Syntaxbeispiele in der Zelle EventDblClick eines Shapes.
  
CALLTHIS("ThisDocument.A",)
  
CALLTHIS("ThisDocument.B",,"Click")
  
CALLTHIS("ThisDocument.C",,"Klicken Sie auf", "OK.")
  

