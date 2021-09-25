---
title: PATHLENGTH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.
ms.openlocfilehash: da00d0b144be5526eaa8d253b7b52a397af68538
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608070"
---
# <a name="pathlength-function"></a>PATHLENGTH Function

Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

PATHLENGTH(** *Section* ** ** *[,segment]* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das auf 1 basierende Segment des zu messenden Pfads.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Double**
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn _kein Abschnitt_ oder _Segment_ vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  
Wenn Sie einen  _Segmentwert_ einschließen, gibt PATHLENGTH nur die Länge dieses Abschnitts zurück. 
  

