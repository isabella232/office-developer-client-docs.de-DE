---
title: PATHLENGTH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405849"
---
# <a name="pathlength-function"></a>PATHLENGTH Function

Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

PATHLENGTH (* * *section* * * * * *[, Segment]* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das auf 1 basierende Segment des zu messenden Pfads.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Double**
  
## <a name="remarks"></a>Bemerkungen

Wenn _section_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  
Wenn Sie einen _Segment_ Wert angeben, gibt PATHLENGTH nur die Länge dieses Segments zurück. 
  

