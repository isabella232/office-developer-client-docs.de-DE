---
title: Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 309d2b3d-dc71-4222-b293-4bfc467b5429
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8bc60dd8241062abb45523393aaf2025ddac03b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614115"
---
# <a name="getting-and-setting-properties-with-getprops-and-setprops"></a>Abrufen und Festlegen von Eigenschaften mit GetProps und SetProps
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Versuchen Sie nach Möglichkeit, eine Eigenschaft mit den Methoden [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps](imapiprop-setprops.md) abzurufen oder zu ändern. Wenn die Eigenschaft, mit der Sie arbeiten, nicht sehr groß ist, sollten diese Methoden angemessen sein. Die andere Alternative besteht darin, mit der [IStream-Schnittstelle](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) aus einem Datenstrom zu lesen oder in einen Datenstrom zu schreiben. Streams können sehr große Eigenschaften erfolgreich verarbeiten, sind aber ein höherer Ressourcenabfluss, da sie die COM-Bibliotheken benötigen. Verwenden Sie die **IStream-Schnittstelle** erst nach einem Fehler beim Aufruf von **IMAPIProp::GetProps** oder **IMAPIProp::SetProps.** 
  

