---
title: Initialisieren von OLE für MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6efe41c79cd85eb844ee19b8c54e200956c9b2a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792680"
---
# <a name="initializing-ole-for-mapi"></a>Initialisieren von OLE für MAPI

  
  
**Betrifft**: Outlook 
  
Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) die OLE-Bibliotheken nicht initialisiert werden. **OleInitialize** globale Daten für die Sitzung initialisiert und bereitet die OLE-Bibliotheken Anrufe annehmen. Informationen zu den aufrufenden **OleInitialize**finden Sie im Windows-SDK.
  

