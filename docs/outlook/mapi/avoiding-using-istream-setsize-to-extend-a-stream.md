---
title: Vermeiden der Verwendung von IStreamSetSize zum Erweitern eines Datenstroms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c4df52e6be76bd7844ed4b16912a4e1d7642edfb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584773"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Vermeiden der Verwendung von IStream::SetSize zum Erweitern eines Datenstroms

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Schreiben in Datenströme ist es manchmal erforderlich, sie zu vergrößern, da ihre ursprüngliche Größe nicht mehr ausreicht. Verwenden Sie die OLE-Methode **IStream::Write,** um dies zu erreichen, anstatt **IStream::SetSize**. **IStream::Write** erweitert den Datenstrom automatisch und macht ** IStream::SetSize ** unnötig. Das Aufrufen von **IStream::Write** ohne **IStream::SetSize** kann bis zu dreimal schneller sein als das Ausführen des **SetSize-Aufrufs** vor dem **Schreiben.**
  

