---
title: RUNADDON-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Führt ein Add-on oder ein Makro in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt aus.
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797966"
---
# <a name="runaddon-function"></a>RUNADDON Function

Führt ein Add-on oder ein Makro in einem Microsoft Visual Basic für Applikationen (VBA)-Projekt aus. 
  
## <a name="syntax"></a>Syntax

RUNADDON (" *String* ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name eines Add-Ons in der **Addons**-Auflistung oder ein Makro in einem VBA-Projekt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn das Projekt des Dokuments, die den RUNADDON-Funktionsaufruf enthält (oder einem anderen Projekt, wenn darauf verwiesen wird) Makro (eine Prozedur ohne Argumente) namens _String_nicht vorhanden ist, wird in Microsoft Visio das Add-on _String_ausgeführt. Wenn kein Add-on mit dem Namen _String_ gefunden werden kann, wird von Visio hat keine Auswirkung und kein Fehler gemeldet. (Mit die **TraceFlags** -Eigenschaft können Sie die Prozeduren und Add-ons, die zum Ausführen von Visio versucht überwachen.) 
  
Wenn Sie eine Prozedur in einem Standardmodul aufrufen, wird empfohlen, mit dem Modulnamen, der die Prozedur (beispielsweise *moduleName.procName*), enthält die Zeichenfolge als Präfix, da mehrere Module eine Prozedur mit dem gleichen Namen aufweisen kann. 
  
Zum Aufrufen einer Prozedur in einem Projekt auf das Projekt des Dokuments, die den RUNADDON-Funktionsaufruf enthält verwenden die Syntax *projName.modName.procName* (Sie müssen im VBA-Projekt ausdrücklich einen Verweis auf *Projektname bezeichnete* festgelegt haben). 
  
> [!NOTE]
>  Ab Visio 2002 kann die RUNADDON-Funktion keine Zeichenfolgen mit beliebigem VBA-Code ausführen. Code, der früher an die RUNADDON-Funktion übergeben wurde, kann in eine Prozedur im VBA-Projekt eines Dokuments verschoben werden, das aus der RUNADDON-Funktion aufgerufen wird. 
  
Weitere Informationen zum Ausführen von Code in Visio finden Sie unter [Informationen zu Sicherheitseinstellungen und zum Ausführen von Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in dieser ShapeSheet-Referenz. 
  
In früheren Visio-Versionen wird diese Funktion in der Form _RUNADDON geschrieben. In Visio, Version 4.0 und höher, können beide Schreibweisen verwendet werden. 
  
## <a name="example-1"></a>Beispiel 1

RUNADDON("Calendar.exe")
  
Startet das Add-on Calendar.exe aufgerufen.
  
## <a name="example-2"></a>Beispiel 2

RUNADDON("Shapes anordnen")
  
Startet das (VSL-implementierte) Add-On Shapes anordnen.
  
## <a name="example-3"></a>Beispiel 3

RUNADDON("ThisDocument.ReportStatistics")
  
Ruft das Makro ReportStatistics im Modul ThisDocument im Dokumentprojekt auf, das diesen Funktionsaufruf enthält. 
  
> [!NOTE]
>  Zum Aufrufen eines Makros im Modul **ThisDocument** müssen Sie der Zeichenfolge wie dargestellt "ThisDocument" voranstellen. 
  
## <a name="example-4"></a>Beispiel 4

RUNADDON (" *ModuleName* . ReportStatistics") 
  
Ruft das Makro ReportStatistics in *ModuleName* im Dokumentprojekt auf, das diesen Funktionsaufruf enthält. 
  

