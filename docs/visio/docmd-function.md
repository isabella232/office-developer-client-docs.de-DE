---
title: DOCMD-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Führt den identifizierten Befehl aus.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413073"
---
# <a name="docmd-function"></a>DOCMD Function

Führt den identifizierten Befehl aus.
  
## <a name="syntax"></a>Syntax

 **DOCMD**( _commandID_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _commandID_ <br/> |Erforderlich  <br/> |**Number** <br/> | Der auszuführende Befehl.  <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Liste der Befehle, die mit der DOCMD-Funktion unterstützt werden, finden Sie im Thema "DoCmd/DOCMD-Befehle" in der Microsoft Visio 2013 Automation Reference. 
  
## <a name="example"></a>Beispiel

 `DOCMD (1312)`
  
Bewirkt, dass das Dialogfeld **Shape-Daten** auf der Benutzeroberfläche angezeigt wird. 
  

