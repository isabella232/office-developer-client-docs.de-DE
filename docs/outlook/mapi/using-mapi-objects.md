---
title: Verwenden von MAPI-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d732efe5276f4756f43b4aca46e1c33d6f103844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329677"
---
# <a name="using-mapi-objects"></a>Verwenden von MAPI-Objekten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clients und Dienstanbieter verwenden MAPI-Objekte, indem sie die Methoden in ihren Schnittstellenimplementierung aufrufen. Nur so können #A0 verwendet werden. Methoden, die von einem Objekt außerhalb einer MAPI-Schnittstelle implementiert werden, sind nicht öffentlich zugänglich. Da alle Schnittstellen eines Objekts über die Vererbung miteinander verknüpft sind, kann der Benutzer eines Objekts Methoden entweder in der Basisschnittstelle oder in einer der geerbten Schnittstellen aufrufen, als gehörten sie zur gleichen Schnittstelle. 
  
Wenn der Benutzer eines Objekts einen Aufruf einer Methode erstellen möchte und dieses Objekt mehrere Schnittstellen implementiert, die sich auf die Vererbung bezogen haben, muss der Benutzer nicht wissen, zu welcher Schnittstelle die Methode gehört. Der Benutzer kann eine der Methoden für jede der Schnittstellen mit einem einzelnen Zeiger auf das Objekt aufrufen. Die folgende Abbildung zeigt beispielsweise, wie eine Clientanwendung ein Ordnerobjekt verwendet. Folder-Objekte implementieren die [IMAPIFolder : IMAPIContainer-Schnittstelle,](imapifolderimapicontainer.md) die indirekt von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) über [IMAPIProp erbt: IUnknown](imapipropiunknown.md) und [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). Ein Client kann eine der **IMAPIProp-Methoden** wie [IMAPIProp::GetProps](imapiprop-getprops.md)und eine der [IMAPIFolder : IMAPIContainer-Methoden](imapifolderimapicontainer.md) wie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)auf dieselbe Weise mit demselben Objektzeiger aufrufen. Ein Client ist sich nicht bewusst oder davon betroffen, dass diese Aufrufe zu unterschiedlichen Schnittstellen gehören.
  
**Kundenverwendung eines Ordnerobjekts**
  
![Clientnutzung eines Ordnerobjekts](media/amapi_40.gif "Clientnutzung eines Ordnerobjekts")
  
Diese Aufrufe werden in Code unterschiedlich übersetzt, je nachdem, ob der Client, der die Aufrufe vor sich führt, in C oder C++ geschrieben ist. Bevor ein Aufruf einer Methode vorgenommen werden kann, muss ein Zeiger auf die Schnittstellenimplementierung abgerufen werden. Schnittstellenzeiger können auf folgende Weise erhalten werden:
  
- Aufrufen einer Methode für ein anderes Objekt.
    
- Aufrufen einer API-Funktion.
    
- Aufrufen der [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) für das Zielobjekt. 
    
MAPI bietet mehrere Methoden und API-Funktionen, die Zeiger auf Schnittstellenimplementierung zurückgeben. Clients können beispielsweise die [IMAPISession::GetMsgStoresTable-Methode](imapisession-getmsgstorestable.md) aufrufen, um einen Zeiger auf ein Tabellenobjekt abzurufen, das über die [IMAPITable : IUnknown-Schnittstelle](imapitableiunknown.md) Zugriff auf Informationen des Nachrichtenspeicheranbieters bietet. Dienstanbieter können die API-Funktion [CreateTable aufrufen,](createtable.md) um einen Zeiger auf ein Tabellendatenobjekt abzurufen. Wenn keine Funktion oder Methode verfügbar ist und Clients oder Dienstanbieter bereits über einen Zeiger auf ein Objekt verfügen, können sie die **QueryInterface-Methode** des Objekts aufrufen, um einen Zeiger auf eine andere der Schnittstellenimplementierung des Objekts abzurufen. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

