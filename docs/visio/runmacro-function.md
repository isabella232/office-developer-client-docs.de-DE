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
description: Ruft ein Makro in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt.
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797963"
---
# <a name="runmacro-function"></a>RUNMACRO Function

Ruft ein Makro in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt. 
  
## <a name="syntax"></a>Syntax

RUNMACRO (** *Makroname* ** [, ** *Projname_opt* **]) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Makroname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name des aufzurufenden Makros.  <br/> |
| _projname_opt_ <br/> |Optional  <br/> |**String** <br/> | Das Projekt, das den Makro enthält.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Projekt angegeben ist, durchsucht Microsoft Visio alle geöffneten Dokumente für eine enthaltenden _Projname_opt_ und Anrufe _Makroname_ in diesem Projekt. Wenn _Projname_opt_ nicht angegeben oder null (""), wird angenommen, dass _Macroname_ im VBA-Projekt des Dokuments werden, die gerade RUNMACRO-Formel enthält. 
  
Die RUNMACRO-Funktion unterscheidet sich von der CALLTHIS-Funktion, darin, dass sie einen Verweis auf die Form nicht erfolgreich überprüft, der das Formel zur _Makroname_Berechnung besitzt. Ebenso wie die CALLTHIS muss die RUNMACRO-Funktion verweisen, um _Projname_opt_ aufrufen können. 
  
 VBA-Code, der aufgerufen wird, wenn die Visio-Instanz eine RUNMACRO-Funktion in einer Formel auswertet, darf das Dokument mit der Zelle, die die Funktion verwendet, nicht schließen, da dies zu einem Anwendungsfehler führt und Visio beendet wird. 
  
Wenn Sie das Dokument mit der Zelle, die die RUNMACRO-Funktion verwendet, schließen müssen, wenden Sie eines der folgenden Verfahren an:
  
- Schließen Sie das Dokument über anderen Code als VBA-Code.
    
- Schließen Sie das Dokument von einem anderen Projekt aus als von jenen, das gerade geschlossen wird.
    
- Fügen Sie Fenster-Nachrichten zum Schließen der Fenster ein, anstatt das Dokument zu schließen.
    
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und Ausführung von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird das Makro MyTest im Klassenmodul ThisDocument des VBA-Projekts aufgerufen, das die RUNMACRO-Formel enthält. 
  
RUNMACRO ("ThisDocument.MyTest") 
  

