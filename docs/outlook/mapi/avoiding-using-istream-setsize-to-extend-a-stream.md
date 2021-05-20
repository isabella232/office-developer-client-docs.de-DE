---
title: Vermeiden der Verwendung von IStreamSetSize zum Erweitern eines Datenstroms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428914"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Vermeiden der Verwendung von IStream::SetSize zum Erweitern eines Datenstroms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Schreiben in Datenströme ist es manchmal erforderlich, sie zu vergrößern, da ihre Anfangsgröße nicht mehr ausreicht. Verwenden Sie die **OLE-Methode IStream::Write,** um dies zu erreichen, anstatt **IStream::SetSize**. **IStream::Write** erweitert den Datenstrom automatisch und macht ** IStream::SetSize ** unnötig. Das **Aufrufen von IStream::Write** ohne **IStream::SetSize** kann bis zu dreimal schneller sein als der **SetSize-Aufruf** vor **Write**.
  

