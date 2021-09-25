---
title: DOOLEVERB-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251421
ms.localizationpriority: medium
ms.assetid: d276c122-6326-75a7-220c-6a78e94e0db0
description: Führt ein Verb für das OLE-Objekt aus.
ms.openlocfilehash: 93f69735dbf1d2ae31f0d8c33306c422ecafbfb7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590282"
---
# <a name="dooleverb-function"></a>DOOLEVERB Function

Führt ein Verb für das OLE-Objekt aus.
  
## <a name="syntax"></a>Syntax

DOOLEVERB(" ** *verb* ** ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _"verb"_ <br/> |Erforderlich  <br/> |**String** <br/> |Die auszuführende Aktion.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In früheren Versionen von Visio wird diese Funktion in der Form _DOOLEVERB angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an. 
  
## <a name="example"></a>Beispiel

DOOLEVERB("bearbeiten")
  
Ruft das Programm auf, aus dem das OLE-Objekt stammt, und öffnet das verknüpfte oder eingebettete Objekt zum Bearbeiten.
  

