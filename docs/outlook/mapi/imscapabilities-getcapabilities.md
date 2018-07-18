---
title: IMSCapabilitiesGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSCapabilities.GetCapabilities
api_type:
- COM
ms.assetid: c77a8ef1-0730-d458-b35f-451d3f450fac
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 27db5f54f6a6feba77308a4a63fe4c16448550cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792609"
---
# <a name="imscapabilitiesgetcapabilities"></a>IMSCapabilities::GetCapabilities

  
  
**Betrifft**: Outlook 
  
Ruft Informationen zu was ein Speicher unterstützt werden kann, basierend auf die angegebene Auswahl.
  
```cpp
ULONG GetCapabilities( 
MSCAP_SELECTOR mscapSelector 
);
```

## <a name="parameters"></a>Parameter

 *mscapSelector* 
  
> [in] Selektor, der angibt, welche Funktionen zurückgegeben.
    
## <a name="return-value"></a>R�ckgabewert

MSCAP_SECURE_FOLDER_HOMEPAGES
  
> Unterstützung für Homepages in einem Speicher nicht standardmäßigen Ordners. Dies kann zurückgegeben werden, wenn **MSCAP_SEL_FOLDER** im *MscapSelector* angegeben ist. 
    
MSCAP_RES_ANNOTATION
  
> Wenn eine Einschränkung ungültige Argumente wie ungültige Eigenschaften enthält, der Informationsspeicher ignoriert die ungültige Argumente und verarbeitet nur die gültigen Argumente. Dies kann zurückgegeben werden, wenn **MSCAP_SEL_RESTRICTION** im *MscapSelector* angegeben ist. 
    
NULL
  
> Jede Funktion basierend auf dem angegebenen Selektor unterstützt der Speicher nicht.
    

