---
title: DOOLEVERB-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
localization_priority: Normal
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Führt eine Aktion für das OLE-Objekt.
ms.openlocfilehash: a7786c3ef2b4039e288596ed367083a4ed3a6c13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796884"
---
# <a name="dooleverb-function"></a>DOOLEVERB Function

Führt eine Aktion für das OLE-Objekt.
  
## <a name="syntax"></a>Syntax

DOOLEVERB ("** *Verb* **") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _"Verb"_ <br/> |Erforderlich  <br/> |**String** <br/> |Die auszuführende Aktion.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In früheren Versionen von Visio wird diese Funktion in der Form _DOOLEVERB angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an. 
  
## <a name="example"></a>Beispiel

DOOLEVERB("edit")
  
Ruft das Programm auf, aus dem das OLE-Objekt stammt, und öffnet das verknüpfte oder eingebettete Objekt zum Bearbeiten.
  

