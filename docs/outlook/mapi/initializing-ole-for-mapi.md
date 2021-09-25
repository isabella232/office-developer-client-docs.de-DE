---
title: Initialisieren von OLE für MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 53b65299-69f8-4fc0-8d9b-f666e814aaac
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 91552ba5a37915ad8a75bd49038e6e90585bd615
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564099"
---
# <a name="initializing-ole-for-mapi"></a>Initialisieren von OLE für MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) auf, um die OLE-Bibliotheken zu initialisieren. **OleInitialize initialisiert** globale Daten für die Sitzung und bereitet die OLE-Bibliotheken auf die Annahme von Aufrufen vor. Informationen zum Aufrufen von **OleInitialize** finden Sie im Windows SDK.
  

