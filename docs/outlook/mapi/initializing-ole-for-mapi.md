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
ms.openlocfilehash: 87310916f4a54b308f0599ec5c1a4a3bfe83c376
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388416"
---
# <a name="initializing-ole-for-mapi"></a>Initialisieren von OLE für MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) die OLE-Bibliotheken nicht initialisiert werden. **OleInitialize** globale Daten für die Sitzung initialisiert und bereitet die OLE-Bibliotheken Anrufe annehmen. Informationen zu den aufrufenden **OleInitialize**finden Sie im Windows-SDK.
  

