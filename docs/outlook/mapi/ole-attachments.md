---
title: OLE-Anlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b95b83ad7eedff577e4c36365c9e451f4b458173
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793291"
---
# <a name="ole-attachments"></a>OLE-Anlagen

  
  
**Betrifft**: Outlook 
  
Anlagen, die OLE-Objekte als OLE-1-Stream-Objekten f�r die Abw�rtskompatibilit�t codiert sind. Wenn das urspr�ngliche Objekt wirklich um ein OLE-2 **IStorage** -Objekt ist, muss das Objekt in einer OLE-1-Stream konvertiert werden soll. Diese Konvertierung erfolgt mithilfe der **OleConvertIStorageToOLESTREAM** -Funktion, die Teil der Win32 OLE-Bibliotheken ist. 
  

