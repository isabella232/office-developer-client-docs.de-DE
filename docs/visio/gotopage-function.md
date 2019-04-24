---
title: GOTOPAGE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
localization_priority: Normal
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Zeigt die Seite mit dem Namen pagename im derzeit aktiven Fenster an.
ms.openlocfilehash: c96585406b6104aeedbe46c35024a4f13bb0953e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302968"
---
# <a name="gotopage-function"></a>GOTOPAGE Function

Zeigt die Seite mit dem Namen *pagename* im derzeit aktiven Fenster an. 
  
## <a name="syntax"></a>Syntax

GOTOPAGE ("* * *Seitenname* * *") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name des Zeichenblatts, zu dem gewechselt werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Fenster die Seite bereits anzeigt, wird dieses Fenster aktiv. Wenn *pagename* nicht vorhanden ist, versucht die anwendung zu https://pagename ** /zu navigieren. Wenn Visio als ein in-Place-Server fungiert, hat die GOTOPAGE-Funktion keine Auswirkung. 
  
Sie können die HYPERLINK-Funktion verwenden, um zu einem beliebigen DOS-, UNC- oder URL-Pfad zu wechseln. 
  
In früheren Visio-Produktversionen wird diese Funktion in der Form _GOTOPAGE angezeigt. In den Visio-Versionen 4.0 und höher werden beide Schreibweisen akzeptiert. 
  

