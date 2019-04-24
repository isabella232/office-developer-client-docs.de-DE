---
title: Vermeiden der Verwendung von IStreamSetSize zum Erweitern eines Streams
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 614bb3d142b7aaabe89223b6ce3552469edfce27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331640"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a>Vermeiden der Verwendung von IStream:: SetSize zum Erweitern eines Streams

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beim Schreiben in Streams ist es manchmal erforderlich, Sie zu vergrößern, da ihre anfängliche Größe nicht mehr ausreicht. Verwenden Sie die OLE-Methode **IStream:: Write** anstelle von **IStream:: SetSize**. **IStream:: Write** erweitert den Stream automatisch, sodass * * IStream:: SetSize * * nicht erforderlich ist. Das Aufrufen von **IStream:: Write** ohne **IStream:: SetSize** kann bis zu dreimal schneller sein als das Ausführen des SetSize-Aufrufs vor dem **Schreiben**. ****
  

