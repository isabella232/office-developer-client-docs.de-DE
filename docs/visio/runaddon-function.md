---
title: RUNADDON-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
ms.localizationpriority: medium
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Führt ein Add-On oder ein Makro in einem Microsoft Visual Basic for Applications (VBA)-Projekt aus.
ms.openlocfilehash: 9f861cc5b118f7146f9d778226720e45fa5aba73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573418"
---
# <a name="runaddon-function"></a>RUNADDON Function

Führt ein Add-On oder ein Makro in einem Microsoft Visual Basic for Applications (VBA)-Projekt aus. 
  
## <a name="syntax"></a>Syntax

RUNADDON(" *string*  ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zeichenfolge_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name eines Add-Ons in der **Addons**-Auflistung oder ein Makro in einem VBA-Projekt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das Projekt des Dokuments, das den RUNADDON-Funktionsaufruf enthält (oder ein anderes Projekt, auf das verwiesen wird), nicht über ein Makro (eine Prozedur ohne Argumente) mit der benannten _Zeichenfolge_ verfügt, führt Microsoft Visio das Add-On mit der benannten _Zeichenfolge_ aus. Wenn keine benannte _Zeichenfolge_ des Add-Ons gefunden werden kann, führt Visio keine Aktion aus und meldet keinen Fehler. (Sie können mit der **TraceFlags**-Eigenschaft die Prozeduren und Add-Ons überwachen, die Visio versucht auszuführen.) 
  
Wenn Sie eine Prozedur in einem Standardmodul aufrufen, wird empfohlen, der Zeichenfolge den Modulnamen vorangestellt zu haben, der die Prozedur enthält (z. B.  *moduleName.procName),* da mehrere Module eine Prozedur mit demselben Namen aufweisen können. 
  
Verwenden Sie zum Aufrufen einer Prozedur in einem anderen Projekt als dem Projekt des Dokuments, das den RUNADDON-Funktionsaufruf enthält, die Syntax  *"projName.modName.procName"*  (Sie müssen in Ihrem VBA-Projekt explizit einen Verweis auf  *"projName"*  festgelegt haben). 
  
> [!NOTE]
>  Ab Visio 2002 kann die RUNADDON-Funktion keine Zeichenfolgen mit beliebigem VBA-Code ausführen. Code, der früher an die RUNADDON-Funktion übergeben wurde, kann in eine Prozedur im VBA-Projekt eines Dokuments verschoben werden, das aus der RUNADDON-Funktion aufgerufen wird. 
  
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
In früheren Visio-Versionen wird diese Funktion in der Form _RUNADDON geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden. 
  
## <a name="example-1"></a>Beispiel 1

RUNADDON("Calendar.exe")
  
Startet ein Add-On mit dem Namen Calendar.exe.
  
## <a name="example-2"></a>Beispiel 2

RUNADDON("Shapes anordnen")
  
Startet das (VSL-implementierte) Add-On Shapes anordnen.
  
## <a name="example-3"></a>Beispiel 3

RUNADDON("ThisDocument.ReportStatistics")
  
Ruft das ReportStatistics-Makro im **Modul "ThisDocument"** im Dokumentprojekt auf, das diesen Funktionsaufruf enthält. 
  
> [!NOTE]
>  Zum Aufrufen eines Makros im Modul **ThisDocument** müssen Sie der Zeichenfolge wie dargestellt "ThisDocument" voranstellen. 
  
## <a name="example-4"></a>Beispiel 4

RUNADDON(" *ModuleName*  . ReportStatistics") 
  
Ruft das ReportStatistics-Makro in  *ModuleName*  im Dokumentprojekt auf, das diesen Funktionsaufruf enthält. 
  

