---
title: CALLOUTTARGETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
ms.openlocfilehash: aeeb919fb2efc175d8e5ce23f464503c13331249
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423013"
---
# <a name="callouttargetref-function"></a>CALLOUTTARGETREF Function

Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

CALLOUTTARGETREF()!
  
### <a name="return-value"></a>Rückgabewert

ShapeSheet-Referenz
  
## <a name="remarks"></a>Hinweise

Wenn es sich bei dem Shape nicht um ein Callout-Shape handelt oder wenn es keinem Ziel-Shape zugeordnet ist, gibt CALLOUTTARGETREF #REF.
  
## <a name="example"></a>Beispiel

CALLOUTTARGETREF()! Height 
  
Gibt den Wert in der Zelle Height des Shapes zurück, das mit der Beschriftung verknüpft ist. 
  

