---
title: Verwenden von IStreamSetSize zum Erweitern eines Stream-Objekts zu vermeiden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 54d352c263fd34bc8494d8d76c76cb22e0bafa58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791372"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Erweitern ein Stream-Objekts mit:: setSize zu vermeiden

  
  
**Betrifft**: Outlook 
  
Beim Schreiben in Streams ist es manchmal notwendig, den sie vergrößern, da ihre ursprüngliche Größe nicht mehr ausreichend ist. Verwenden Sie die OLE-Methode **IStream::Write** dazu statt **:: setSize**. **IStream::Write** erweitert automatisch den Stream tätigen **:: setSize ** nicht erforderlich. Aufrufen von **IStream::Write** ohne **:: setSize** kann bis zu drei Mal schneller als vornehmen der **SetSize** aufrufen, bevor Sie **Schreiben**sein.
  

