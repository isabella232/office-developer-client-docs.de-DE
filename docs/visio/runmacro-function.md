---
title: RUNMACRO-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
ms.localizationpriority: medium
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Ruft ein Makro in einem VBA-Projekt (Microsoft Visual Basic for Applications) auf.
ms.openlocfilehash: b3d84f672913841d609320a3af7e3b9734291117
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598185"
---
# <a name="runmacro-function"></a>RUNMACRO Function

Ruft ein Makro in einem VBA-Projekt (Microsoft Visual Basic for Applications) auf. 
  
## <a name="syntax"></a>Syntax

RUNMACRO (** *Makroname* ** [, ** *projname_opt* ** ]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Makroname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name des aufzurufenden Makros.  <br/> |
| _projname_opt_ <br/> |Optional  <br/> |**String** <br/> | Das Projekt, das den Makro enthält.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn ein Projekt angegeben ist, überprüft Microsoft Visio alle geöffneten Dokumente nach dem Dokument, das _projname_opt_ enthält, und ruft den _Makronamen_ in diesem Projekt auf. Wenn  _projname_opt_ ausgelassen wird oder null (""), wird angenommen, dass sich der  _Makroname_ im VBA-Projekt des Dokuments befindet, das die ausgewertete RUNMACRO-Formel enthält. 
  
Die RUNMACRO-Funktion unterscheidet sich von der CALLTHIS-Funktion darin, dass sie keinen Verweis auf das Shape übergibt, das die Formel besitzt, die als  _Makroname_ ausgewertet wird. Wie CALLTHIS erfordert die RUNMACRO-Funktion keinen Verweis auf  _projname_opt,_ um sie aufzurufen. 
  
 VBA-Code, der aufgerufen wird, wenn die Visio-Instanz eine RUNMACRO-Funktion in einer Formel auswertet, darf das Dokument mit der Zelle, die die Funktion verwendet, nicht schließen, da dies zu einem Anwendungsfehler führt und Visio beendet wird. 
  
Wenn Sie das Dokument mit der Zelle, die die RUNMACRO-Funktion verwendet, schließen müssen, wenden Sie eines der folgenden Verfahren an:
  
- Schließen Sie das Dokument über anderen Code als VBA-Code.
    
- Schließen Sie das Dokument von einem anderen Projekt aus als von jenem, das gerade geschlossen wird.
    
- Fügen Sie Fenster-Nachrichten zum Schließen der Fenster ein, anstatt das Dokument zu schließen.
    
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird das Makro MyTest im Klassenmodul ThisDocument des VBA-Projekts aufgerufen, das die RUNMACRO-Formel enthält. 
  
RUNMACRO ("ThisDocument.MyTest") 
  

