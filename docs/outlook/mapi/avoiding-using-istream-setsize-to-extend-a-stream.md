---
title: Verwenden von IStreamSetSize zum Erweitern eines Stream-Objekts zu vermeiden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9245d4913c2832b8c942093e65cf088643a1947c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592080"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Vermeiden der Verwendung von IStream::SetSize zum Erweitern eines Streams

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beim Schreiben in Streams ist es manchmal notwendig, den sie vergrößern, da ihre ursprüngliche Größe nicht mehr ausreichend ist. Verwenden Sie die OLE-Methode **IStream::Write** dazu statt **:: setSize**. **IStream::Write** erweitert automatisch den Stream tätigen **:: setSize ** nicht erforderlich. Aufrufen von **IStream::Write** ohne **:: setSize** kann bis zu drei Mal schneller als vornehmen der **SetSize** aufrufen, bevor Sie **Schreiben**sein.
  

