---
title: CALLTHIS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
ms.localizationpriority: medium
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Ruft eine Prozedur in einem VBA-Projekt (Microsoft Visual Basic for Applications) auf.
ms.openlocfilehash: 7dff3b6b49eb828b5c73f4aa98da2d5c460a84d4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560081"
---
# <a name="callthis-function"></a>CALLTHIS Function

Ruft eine Prozedur in einem VBA-Projekt (Microsoft Visual Basic for Applications) auf.
  
## <a name="syntax"></a>Syntax

CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Prozedur_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name der Prozedur, die aufgerufen werden soll.  <br/> |
| _Projekt_ <br/> |Optional  <br/> |**String** <br/> |Das Projekt, das die Prozedur enthält.  <br/> |
| _arg_ <br/> |Optional  <br/> |**Number, String, Date oder Currency** <br/> |Wird als Parameter an die Prozedur übergeben,  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Im VBA-Projekt wird  *die Prozedur*  wie folgt definiert: 
  
procedure(*vsoShape* As Visio. Shape [arg1 As type, arg2 As type...]) 
  
dabei ist  *vsoShape*  ein Verweis auf das **Shape-Objekt,** das die ausgewertete CALLTHIS-Formel enthält, und  _arg1_,  *arg2*  ... sind die in dieser Formel angegebenen Argumente. 
  
Beachten Sie, dass  *vsoShape*  dem Argument "this" ähnelt, das an eine C++-Memberprozedur übergeben wird. daher der Name "CALLTHIS". Tatsächlich kann eine Zelle, die eine Formel enthält, die CALLTHIS enthält, wie folgt gelesen werden: "Rufen Sie diese Prozedur auf, und übergeben Sie ihr einen Verweis auf mein Shape." 
  
Wenn _das Projekt_ angegeben ist, überprüft Microsoft Visio alle geöffneten Dokumente nach dem _Projekt,_ das das Projekt enthält, und ruft _die Prozedur_ in diesem Projekt auf. Wenn _das Projekt_ ausgelassen wird oder null (""), nimmt Visio an, dass sich die _Prozedur_ im VBA-Projekt des Dokuments befindet, das die ausgewertete CALLTHIS-Formel enthält. 
  
Zahlen in  _arg1_,  _arg2..._ werden in externen Einheiten übergeben. Wenn Sie z. B. den Wert der Zelle Height aus einer 3 cm hohen Form übergeben, wird 3 übergeben. Um unterschiedliche Einheiten mit einer Zahl zu übergeben, verwenden Sie die FORMATEX-Funktion oder explizit Coerce-Einheiten, indem Sie ein Null-Zahleneinheitspaar hinzufügen, z. B. 0 ft + Height. 
  
Das zweite Komma in der CALLTHIS-Funktion ist optional. Es entspricht der Anzahl zusätzlicher Parameter, die der Prozedur hinzugefügt werden. Wenn Sie keine zusätzlichen Parameter verwenden, außer  `(vsoShape as Visio.Shape)` , fügen Sie nicht das zweite Komma hinzu; verwenden Sie CALLTHIS("",). Wenn Sie beispielsweise zwei zusätzliche Parameter hinzufügen, verwenden Sie CALLTHIS("",,,). 
  
Die CALLTHIS-Funktion wird immer als 0 ausgewertet, und der Aufruf der  _Prozedur_ findet während der Leerlaufzeit nach Abschluss des Neuberechnungsprozesses statt.  _procedure_ kann einen Wert zurückgeben, der jedoch von Visio ignoriert wird.  _Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called _procedure_,unless you want to overwrite the CALLTHIS formula.
  
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

Verwenden Sie das folgende Verfahren im *ThisDocument-Klassenmodul.* 
  
Verwenden Sie mit den oben beschriebenen Prozeduren eines der folgenden Syntaxbeispiele in der Zelle EventDblClick eines Shapes.
  
CALLTHIS("ThisDocument.A",)
  
CALLTHIS("ThisDocument.B",,"Click")
  
CALLTHIS("ThisDocument.C",,"Klicken Sie auf", "OK.")
  

