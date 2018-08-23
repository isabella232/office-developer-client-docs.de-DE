---
title: Initialisieren von OLE für MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd279c17574ce73b42d5e07e96ac817af71dc700
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589805"
---
# <a name="initializing-ole-for-mapi"></a>Initialisieren von OLE für MAPI

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) die OLE-Bibliotheken nicht initialisiert werden. **OleInitialize** globale Daten für die Sitzung initialisiert und bereitet die OLE-Bibliotheken Anrufe annehmen. Informationen zu den aufrufenden **OleInitialize**finden Sie im Windows-SDK.
  

