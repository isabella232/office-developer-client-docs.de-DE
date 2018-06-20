---
title: Verwenden von MAPI-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e342c1bd-8bee-4b02-a93f-e3941f4716c1
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a355faf85a44f6257b77b7171aa965faabf57fe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795833"
---
# <a name="using-mapi-objects"></a>Verwenden von MAPI-Objekten

**Betrifft**: Outlook 
  
Clients und -Dienstanbieter verwenden MAPI-Objekten durch Aufrufen der Methoden in ihren schnittstellenimplementierungen. Dies ist die einzige Möglichkeit, MAPI-Objekten verwendet werden können. Methoden, die von einem Objekt außerhalb einer MAPI-Schnittstelle implementiert sind werden nicht öffentlich zugegriffen. Da ein Objekt Schnittstellen über Vererbung verknüpft sind, kann Benutzer ein Objekt Methoden in der Basis-Schnittstelle oder eines der geerbten Schnittstellen aufrufen, als ob sie die gleiche Benutzeroberfläche angehören. 
  
Wenn ein Objekt einzeln tätigen einen Anruf an eine Methode, und dieses Objekt durch Vererbung bezogene mehrere Schnittstellen implementiert, muss der Benutzer nicht wissen, welche Schnittstelle die Methode gehört. Der Benutzer kann eine der Methoden auf einer Schnittstelle mit einem einzelnen Zeiger auf das Objekt aufrufen. Die folgende Abbildung zeigt, wie eine Clientanwendung ein Folder-Objekt verwendet. Folder-Objekten Implementieren der [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) -Schnittstelle, die von [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indirekt über erbt [IMAPIProp: IUnknown](imapipropiunknown.md) und [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). Ein Client kann eine der Methoden **IMAPIProp** wie [IMAPIProp::GetProps](imapiprop-getprops.md), und eine der Aufrufen der [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) Methoden, wie [IMAPIFolder::CreateMessage](imapifolder-createmessage.md), auf die gleiche Weise mit dem gleichen Objektzeiger. Ein Client ist nicht kennen oder betroffenen durch die Tatsache, dass diese Anrufe zu verschiedenen Schnittstellen gehören.
  
**Clientverwendung eines Ordnerobjekts**
  
![Client zu verwenden, der ein Folder-Objekt] (media/amapi_40.gif "Client zu verwenden, der ein Folder-Objekt")
  
Bei diesen anrufen übersetzen in Code unterschiedlich, je nachdem, ob der Client, die Anrufe in C oder C++ geschrieben ist. Bevor eine beliebige eine Methode aufgerufen werden kann, muss ein Zeiger auf die Implementierung des abgerufen werden. Schnittstellenzeiger erhalten Sie folgendermaßen:
  
- Das Aufrufen einer Methode für ein anderes Objekt.
    
- Aufrufen einer API-Funktion.
    
- Aufrufen der [QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode für das Zielobjekt. 
    
MAPI bietet mehrere Methoden und API-Funktionen, die Zeiger auf schnittstellenimplementierungen zurückgeben. Clients können beispielsweise die [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode, um einen Zeiger auf ein Table-Objekt abzurufen, das Zugriff auf Nachricht Store Anbieterinformationen über bietet Aufrufen der [IMAPITable: IUnknown](imapitableiunknown.md) Schnittstelle. Dienstanbieter können die API-Funktion [CreateTable](createtable.md) einen Zeiger auf ein Table-Datenobjekt abrufen aufrufen. Wenn es keine Funktion oder Methode verfügbar ist und -Clients oder Dienstanbieter bereits einen Zeiger auf ein Objekt ist, können sie das Objekt **QueryInterface** -Methode zum Abrufen eines Zeigers auf ein anderes schnittstellenimplementierungen das Objekt aufrufen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

