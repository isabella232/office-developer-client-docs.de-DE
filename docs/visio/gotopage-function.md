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
description: Zeigt die Seite, die den Namen Pagename in das derzeit aktive Fenster hat.
ms.openlocfilehash: 67f8a79b854fd6f2ae47e39877ffcdbe4a1be5cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797117"
---
# <a name="gotopage-function"></a>GOTOPAGE Function

Zeigt die Seite, die den Namen *Pagename* in das derzeit aktive Fenster hat. 
  
## <a name="syntax"></a>Syntax

GOTOPAGE ("** *Pagename* **") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _pageName_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name des Zeichenblatts, zu dem gewechselt werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn ein Fenster bereits die Seite anzeigt, wird dieses Fenster aktiviert. Wenn *Zeichenblattname* nicht vorhanden ist, wird die Anwendung zum Navigieren zu http:// *Pagename* versucht /. Wenn Visio als in-Place-Server fungiert, hat die GOTOPAGE-Funktion keine Auswirkung. 
  
Sie können die HYPERLINK-Funktion verwenden, um zu einem beliebigen DOS-, UNC- oder URL-Pfad zu wechseln. 
  
In früheren Visio-Produktversionen wird diese Funktion in der Form _GOTOPAGE angezeigt. In den Visio-Versionen 4.0 und höher werden beide Schreibweisen akzeptiert. 
  

