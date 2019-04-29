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
description: Führt ein Verb für das OLE-Objekt aus.
ms.openlocfilehash: c339d03a00afdf7f777bb0624ddb8fa75f277e05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435662"
---
# <a name="dooleverb-function"></a>DOOLEVERB Function

Führt ein Verb für das OLE-Objekt aus.
  
## <a name="syntax"></a>Syntax

DOOLEVERB ("* * *Verb* * *") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Verb_ <br/> |Erforderlich  <br/> |**String** <br/> |Die auszuführende Aktion.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

In früheren Versionen von Visio wird diese Funktion in der Form _DOOLEVERB angezeigt. Die Visio-Versionen 4.0 und höher nehmen beide Schreibweisen an. 
  
## <a name="example"></a>Beispiel

DOOLEVERB ("Bearbeiten")
  
Ruft das Programm auf, aus dem das OLE-Objekt stammt, und öffnet das verknüpfte oder eingebettete Objekt zum Bearbeiten.
  

