---
title: Verwenden von MAPI-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ffa5403121ba86d113647e4da47cdfd8b18eb71
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619491"
---
# <a name="using-mapi-objects"></a>Verwenden von MAPI-Objekten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients und Dienstanbieter verwenden MAPI-Objekte, indem sie die Methoden in ihren Schnittstellenimplementierungen aufrufen. Nur so können MAPI-Objekte verwendet werden. Methoden, die von einem Objekt außerhalb einer MAPI-Schnittstelle implementiert werden, sind nicht öffentlich zugänglich. Da alle Schnittstellen eines Objekts durch Vererbung miteinander verknüpft sind, kann der Benutzer eines Objekts Methoden entweder in der Basisschnittstelle oder in einer der geerbten Schnittstellen aufrufen, als ob sie zur gleichen Schnittstelle gehören. 
  
Wenn der Benutzer eines Objekts eine Methode aufrufen möchte und dieses Objekt mehrere Schnittstellen implementiert, die sich auf vererbungsbezogene Schnittstellen beziehen, muss der Benutzer nicht wissen, zu welcher Schnittstelle die Methode gehört. Der Benutzer kann eine der Methoden auf einer beliebigen Schnittstelle mit einem einzigen Zeiger auf das Objekt aufrufen. Die folgende Abbildung zeigt beispielsweise, wie eine Clientanwendung ein Ordnerobjekt verwendet. Folder-Objekte implementieren die [IMAPIFolder : IMAPIContainer-Schnittstelle,](imapifolderimapicontainer.md) die indirekt von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) über [IMAPIProp erbt: IUnknown](imapipropiunknown.md) und [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). Ein Client kann eine der **IMAPIProp-Methoden,** z. B. [IMAPIProp::GetProps,](imapiprop-getprops.md)und eine der [IMAPIFolder : IMAPIContainer-Methoden,](imapifolderimapicontainer.md) z. B. [IMAPIFolder::CreateMessage,](imapifolder-createmessage.md)auf die gleiche Weise mit demselben Objektzeiger aufrufen. Ein Client ist sich der Tatsache, dass diese Aufrufe zu unterschiedlichen Schnittstellen gehören, nicht bewusst oder ist davon nicht betroffen.
  
**Kundenverwendung eines Ordnerobjekts**
  
![Kundenverwendung eines Ordnerobjekts](media/amapi_40.gif "Kundenverwendung eines Ordnerobjekts")
  
Diese Aufrufe werden in Code anders übersetzt, je nachdem, ob der Client, der die Aufrufe durchführt, in C oder C++ geschrieben ist. Bevor ein Aufruf einer Methode ausgeführt werden kann, muss ein Zeiger auf die Schnittstellenimplementierungen abgerufen werden. Schnittstellenzeiger können auf folgende Weise abgerufen werden:
  
- Aufrufen einer Methode für ein anderes Objekt.
    
- Aufrufen einer API-Funktion.
    
- Aufrufen der [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) für das Zielobjekt. 
    
MAPI stellt mehrere Methoden und API-Funktionen bereit, die Zeiger auf Schnittstellenimplementierungen zurückgeben. Clients können beispielsweise die [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) aufrufen, um einen Zeiger auf ein Tabellenobjekt abzurufen, das über die [IMAPITable : IUnknown-Schnittstelle](imapitableiunknown.md) Zugriff auf Nachrichtenspeicheranbieterinformationen bietet. Dienstanbieter können die API-Funktion [CreateTable](createtable.md) aufrufen, um einen Zeiger auf ein Tabellendatenobjekt abzurufen. Wenn keine Funktion oder Methode verfügbar ist und Clients oder Dienstanbieter bereits über einen Zeiger auf ein Objekt verfügen, können sie die **QueryInterface-Methode** des Objekts aufrufen, um einen Zeiger auf eine andere Schnittstellenimplementierung des Objekts abzurufen. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

