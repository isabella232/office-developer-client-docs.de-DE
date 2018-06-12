---
title: PATHLENGTH-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797604"
---
# <a name="pathlength-function"></a>PATHLENGTH Function

Gibt die Länge des Pfads zurück, der im angegebenen Abschnitt "Geometrie" definiert ist.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010 
  
## <a name="syntax"></a>Syntax

PATHLENGTH (** *Abschnitt* ** ** *[, Segment]* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Abschnitt "Geometrie", der den Pfad darstellt, angegeben mit einer Referenz auf dessen Zelle "Path" (z. B. Geometrie1.Path).  <br/> |
| _Segment_ <br/> |Optional  <br/> |**Integer** <br/> |Das auf 1 basierende Segment des zu messenden Pfads.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

 **Double**
  
## <a name="remarks"></a>Bemerkungen

Wenn _Section_ oder _Segment_ nicht vorhanden ist, gibt Microsoft Visio #REF! zurück. 
  
Wenn Sie einen Wert für _Segment_ eingeschlossen, gibt PATHLENGTH die Länge dieses Abschnitts nur zurück. 
  

