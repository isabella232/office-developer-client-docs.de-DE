---
title: RUNMACRO-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Ruft ein Makro in einem VBA-Projekt (Microsoft Visual Basic für Applikationen) auf.
ms.openlocfilehash: 77045bd67fe9be9aab14e73199b33b93c6d70c2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428088"
---
# <a name="runmacro-function"></a>RUNMACRO Function

Ruft ein Makro in einem VBA-Projekt (Microsoft Visual Basic für Applikationen) auf. 
  
## <a name="syntax"></a>Syntax

RunMacro (* * *Makroname* * * [, * * *projname_opt* * *]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Makroname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name des aufzurufenden Makros.  <br/> |
| _projname_opt_ <br/> |Optional  <br/> |**String** <br/> | Das Projekt, das den Makro enthält.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Projekt angegeben wird, scannt Microsoft Visio alle geöffneten Dokumente für diejenige, die _projname_opt_ enthält, __ und ruft Makroname in diesem Projekt auf. Wenn _projname_opt_ ausgelassen oder NULL ("") ist, __ wird Makroname davon ausgegangen, dass es sich im VBA-Projekt des Dokuments befindet, das die RUNMACRO-Formel enthält, die ausgewertet wird. 
  
Die RUNMACRO-Funktion unterscheidet sich von der CALLTHIS-Funktion dadurch, dass Sie keinen Verweis auf die Form übergibt, die die __ zu bewertende Formel besitzt. Wie CALLTHIS erfordert die RUNMACRO-Funktion keinen Verweis auf _projname_opt_ , um Sie aufzurufen. 
  
 VBA-Code, der aufgerufen wird, wenn die Visio-Instanz eine RUNMACRO-Funktion in einer Formel auswertet, darf das Dokument mit der Zelle, die die Funktion verwendet, nicht schließen, da dies zu einem Anwendungsfehler führt und Visio beendet wird. 
  
Wenn Sie das Dokument mit der Zelle, die die RUNMACRO-Funktion verwendet, schließen müssen, wenden Sie eines der folgenden Verfahren an:
  
- Schließen Sie das Dokument über anderen Code als VBA-Code.
    
- Schließen Sie das Dokument von einem anderen Projekt aus als von jenem, das gerade geschlossen wird.
    
- Fügen Sie Fenster-Nachrichten zum Schließen der Fenster ein, anstatt das Dokument zu schließen.
    
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird das Makro MyTest im Klassenmodul ThisDocument des VBA-Projekts aufgerufen, das die RUNMACRO-Formel enthält. 
  
RUNMACRO ("ThisDocument.MyTest") 
  

