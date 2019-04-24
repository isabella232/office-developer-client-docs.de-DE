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
  
Clients und Dienstanbieter verwenden MAPI-Objekte, indem Sie die Methoden in ihren Schnittstellenimplementierungen aufrufen. Dies ist die einzige Möglichkeit, MAPI-Objekte zu verwenden; Methoden, die von einem Objekt außerhalb einer MAPI-Schnittstelle implementiert werden, sind nicht öffentlich zugänglich. Da alle Schnittstellen eines Objekts durch Vererbung verknüpft sind, kann der Benutzer eines Objekts Methoden in der Basisschnittstelle oder einer der geerbten Schnittstellen aufrufen, als ob Sie zur gleichen Schnittstelle gehören. 
  
Wenn der Benutzer eines Objekts einen Aufruf an eine Methode durchführen möchte und dieses Objekt mehrere Schnittstellen implementiert, die durch Vererbung verknüpft sind, muss der Benutzer nicht wissen, zu welcher Schnittstelle die Methode gehört. Der Benutzer kann eine beliebige Methode auf einer beliebigen Schnittstelle mit einem einzelnen Zeiger auf das Objekt aufrufen. Die folgende Abbildung zeigt beispielsweise, wie eine Clientanwendung ein Folder-Objekt verwendet. Folder-Objekte implementieren die [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) -Schnittstelle, die von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) indirekt über [IMAPIProp: IUnknown](imapipropiunknown.md) und [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)erbt. Ein Client kann eine der **IMAPIProp** -Methoden wie [IMAPIProp::](imapiprop-getprops.md)GetProps und eine der [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) -Methoden wie [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md)auf die gleiche Weise mit demselben Objektzeiger aufrufen. Ein Client ist nicht bekannt oder davon betroffen, dass diese Aufrufe zu unterschiedlichen Schnittstellen gehören.
  
**Kundenverwendung eines Ordnerobjekts**
  
![Client Verwendung eines Folder-Objekts] (media/amapi_40.gif "Client Verwendung eines Folder-Objekts")
  
Diese Aufrufe werden in Code unterschiedlich übersetzt, je nachdem, ob der Client, der die Aufrufe durchführt, in C oder C++ geschrieben wird. Bevor ein Aufruf einer Methode ausgeführt werden kann, muss ein Zeiger auf die Schnittstellenimplementierung abgerufen werden. Schnittstellenzeiger können auf folgende Arten abgerufen werden:
  
- Aufrufen einer Methode für ein anderes Objekt.
    
- Aufrufen einer API-Funktion.
    
- Aufrufen der [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) -Methode für das Zielobjekt. 
    
MAPI bietet mehrere Methoden und API-Funktionen, die Zeiger auf Schnittstellenimplementierungen zurückgeben. Clients können beispielsweise die [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) -Methode aufrufen, um einen Zeiger auf ein Table-Objekt abzurufen, das den Zugriff auf Informationen des Nachrichtenspeicher Anbieters über die [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle ermöglicht. Dienstanbieter können die API-Funktion [Create](createtable.md) Table aufrufen, um einen Zeiger auf ein Tabellendaten Objekt abzurufen. Wenn keine Funktion oder Methode verfügbar ist und Clients oder Dienstanbieter bereits über einen Zeiger auf ein Objekt verfügen, können Sie die **QueryInterface** -Methode des Objekts aufrufen, um einen Zeiger auf eine andere der Schnittstellenimplementierungen des Objekts abzurufen. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über MAPI-Objekte und-Schnittstellen](mapi-object-and-interface-overview.md)

