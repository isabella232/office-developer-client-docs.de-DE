---
title: Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7d11f69c6da8560f5879ebc38498d852486bed8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299398"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Versuchen Sie nach Möglichkeit, eine Eigenschaft mit den Methoden [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPIProp::](imapiprop-setprops.md) SetProps abzurufen oder zu ändern. Wenn die Eigenschaft, mit der Sie arbeiten, sehr umfangreich ist, sollten diese Methoden angemessen sein. Die andere Alternative besteht darin, in einen Stream mit der [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle zu lesen oder zu schreiben. Datenströme können sehr große Eigenschaften erfolgreich behandeln, aber Sie sind ein größerer Ressourcenabfluss, da Sie die COM-Bibliotheken benötigen. Verwenden Sie die **IStream** -Schnittstelle nur nach dem Aufruf von **IMAPIProp::** GetProps oder **IMAPIProp::** SetProps schlägt fehl. 
  

