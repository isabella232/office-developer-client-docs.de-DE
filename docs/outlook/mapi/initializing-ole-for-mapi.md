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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317227"
---
# <a name="initializing-ole-for-mapi"></a>Initialisieren von OLE für MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wenn Sie auch OLE verwenden, rufen Sie die OLE-Funktion [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) auf, um die OLE-Bibliotheken zu initialisieren. **OleInitialize** initialisiert globale Daten für die Sitzung und bereitet die OLE-Bibliotheken auf die Annahme von Anrufen vor. Informationen zum Aufrufen von **OleInitialize** finden Sie im Windows SDK.
  

