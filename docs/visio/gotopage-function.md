---
title: GOTOPAGE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251432
ms.localizationpriority: medium
ms.assetid: b131badf-1656-132e-0aae-eeedb917ba7a
description: Zeigt die Seite mit dem Namen des Seitennamens im derzeit aktiven Fenster an.
ms.openlocfilehash: dfbaff34211d5df467d5ff378df9e37ec0e2e3d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554761"
---
# <a name="gotopage-function"></a>GOTOPAGE Function

Zeigt die Seite mit dem Namen  *des Seitennamens*  im derzeit aktiven Fenster an. 
  
## <a name="syntax"></a>Syntax

GOTOPAGE(" ** *pagename* ** ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _pagename_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name des Zeichenblatts, zu dem gewechselt werden soll.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Seite bereits in einem Fenster angezeigt wird, wird dieses Fenster aktiv. Wenn kein  *Seitenname*  vorhanden ist, versucht die Anwendung, zu https://  *Seitennamen*  /zu navigieren. Wenn Visio als in-place-Server fungiert, hat die GOTOPAGE-Funktion keine Auswirkung. 
  
Sie können die HYPERLINK-Funktion verwenden, um zu einem beliebigen DOS-, UNC- oder URL-Pfad zu wechseln. 
  
In früheren Visio-Produktversionen wird diese Funktion in der Form _GOTOPAGE angezeigt. In den Visio-Versionen 4.0 und höher werden beide Schreibweisen akzeptiert. 
  

