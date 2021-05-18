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
description: Ruft eine Prozedur in einem Microsoft Visual Basic for Applications (VBA)-Projekt auf.
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413815"
---
# <a name="callthis-function"></a>CALLTHIS Function

Ruft eine Prozedur in einem Microsoft Visual Basic for Applications (VBA)-Projekt auf.
  
## <a name="syntax"></a>Syntax

CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Prozedur_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name der Prozedur, die aufgerufen werden soll.  <br/> |
| _project_ <br/> |Optional  <br/> |**String** <br/> |Das Projekt, das die Prozedur enthält.  <br/> |
| _arg_ <br/> |Optional.  <br/> |**Number, String, Date oder Currency** <br/> |Wird als Parameter an die Prozedur übergeben,  <br/> |
   
## <a name="remarks"></a>Hinweise

Im VBA-Projekt  *wird die Prozedur*  wie folgt definiert: 
  
procedure(*vsoShape* As Visio. Shape [arg1 As type, arg2 As type...]) 
  
dabei  *ist vsoShape*  ein Verweis auf das **Shape-Objekt,** das die ausgewertete CALLTHIS-Formel enthält, und  _arg1_,  *arg2*  ... sind die in dieser Formel angegebenen Argumente. 
  
Beachten  *Sie, dass vsoShape*  dem Argument "this" sehr ähnlich ist, das an eine C++-Memberprozedur übergeben wird. daher der Name "CALLTHIS". Tatsächlich kann eine Zelle, die eine Formel enthält, die CALLTHIS enthält, wie folgt gelesen werden: "Rufen Sie diese Prozedur auf, und übergeben Sie ihr einen Verweis auf mein Shape." 
  
Wenn _Project_ angegeben ist, überprüft Microsoft Visio alle geöffneten Dokumente auf das Projekt, das das Projekt enthält, und ruft _die_ Prozedur in diesem Projekt auf.  Wenn _project_ ausgelassen oder null (""), wird  Visio prozedur im #A0 des Dokuments angenommen, das die #A1 enthält, die ausgewertet wird. 
  
Zahlen in  _arg1_,  _arg2..._ werden in externen Einheiten übergeben. Wenn Sie beispielsweise den Wert der Zelle Height von einer 3 cm hohen Form übergeben, wird 3 übergeben. Um verschiedene Einheiten mit einer Zahl zu übergeben, verwenden Sie die FORMATEX-Funktion oder explizit Koerceeinheiten, indem Sie ein Nullzeichen-Einheitenpaar hinzufügen, z. B. 0 ft + Height. 
  
Das zweite Komma in der CALLTHIS-Funktion ist optional. Es entspricht der Anzahl zusätzlicher Parameter, die der Prozedur hinzugefügt werden. Wenn Sie keine zusätzlichen Parameter verwenden, außer , fügen Sie nicht das  `(vsoShape as Visio.Shape)` zweite Komma hinzu; verwenden Sie CALLTHIS("",). Wenn Sie beispielsweise zwei zusätzliche Parameter hinzufügen, verwenden Sie CALLTHIS("",,,). 
  
Die CALLTHIS-Funktion wird immer als 0  ausgewertet, und der Aufruf der Prozedur erfolgt während der Leerlaufzeit nach Abschluss des Neuberechnungsprozesses.  _procedure_ kann einen Wert zurückgeben, der jedoch von Visio ignoriert wird.  _Procedure_ gibt einen Wert zurück, den Visio erkennen kann, indem Sie die Formel oder das Ergebnis einer anderen Zelle im Dokument festlegen, aber nicht die Zelle, die prozedur aufgerufen _hat,_ es sei denn, Sie möchten die CALLTHIS-Formel überschreiben.
  
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
  

