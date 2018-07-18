---
title: CALLOUTTARGETREF-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67cfd32-5911-d8e9-dd51-fd4885dd2b0d
description: Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
ms.openlocfilehash: 1b0cb7c6737a810a0ade65f19afaff7bb4b9f616
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796550"
---
# <a name="callouttargetref-function"></a>CALLOUTTARGETREF Function

Gibt eine Shape-Referenz auf das übergeordnete Shape des Beschriftungs-Shapes zurück.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

CALLOUTTARGETREF()!
  
### <a name="return-value"></a>R�ckgabewert

ShapeSheet-Referenz
  
## <a name="remarks"></a>Bemerkungen

Wenn die Form nicht um eine Beschriftung-Shape ist oder wenn es nicht mit einem übergeordneten Shape verknüpft ist, gibt CALLOUTTARGETREF #REF zurück.
  
## <a name="example"></a>Beispiel

CALLOUTTARGETREF()!Height 
  
Gibt den Wert in der Zelle Height des Shapes zurück, das mit der Beschriftung verknüpft ist. 
  

