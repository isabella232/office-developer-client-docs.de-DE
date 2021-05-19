---
title: Festlegen von Adressbuchoptionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417343"
---
# <a name="setting-address-book-options"></a>Festlegen von Adressbuchoptionen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können drei Eigenschaften festlegen, die Optionen für die Verwendung des Adressbuchs beschreiben:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    Die **PR_AB_SEARCH_PATH-Eigenschaft** wird von [IAddrBook::ResolveName](iaddrbook-resolvename.md) verwendet, um die Container zu bestimmen, die an der Namensauflösung beteiligt sein sollen, und die Reihenfolge, in der sie beteiligt werden sollen. Für jeden Container in **PR_AB_SEARCH_PATH** **ruft IAddrBook::ResolveName** seine [IABContainer::ResolveNames-Methode](iabcontainer-resolvenames.md) auf. Container am Anfang der **PR_AB_SEARCH_PATH** werden vor Containern am Ende der **PR_AB_SEARCH_PATH.** 
    
    Die Suchreihenfolge in **PR_AB_SEARCH_PATH** wird mithilfe einer [SRowSet-Struktur](srowset.md) angegeben, derselben Struktur, die zum Darstellen von Zeilen in einer Tabelle verwendet wird. Sie können den aktuellen Suchpfad anzeigen, indem Sie die [IAddrBook::GetSearchPath-Methode](iaddrbook-getsearchpath.md) aufrufen und ändern, indem Sie die [IAddrBook::SetSearchPath-Methode](iaddrbook-setsearchpath.md) aufrufen. 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    Die **PR_AB_DEFAULT_DIR** ist die Eintrags-ID des Adressbuchcontainers, der beim Anzeigen des Adressbuchs zunächst angezeigt werden soll. Die Standardverzeichniseinstellung bleibt in Kraft, bis Sie sie durch Aufrufen der [IAddrBook::SetDefaultDir-Methode](iaddrbook-setdefaultdir.md) ändern. Sie können das Standardverzeichnis anzeigen, indem Sie die [IAddrBook::GetDefaultDir-Methode](iaddrbook-getdefaultdir.md) aufrufen. 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Diese drei Eigenschaften sind besonders, da Sie nicht mit den standardmäßigen **IMAPIProp-Methoden arbeiten** können. Stattdessen müssen Sie **IAddrBook-Methoden** verwenden. Da keine dieser Eigenschaften mit **IMAPIProp::SetProps** geändert werden kann, müssen Sie **IMAPIProp::SaveChanges** nicht aufrufen, um Änderungen dauerhaft vorzunehmen. Änderungen, die über die **IAddrBook-Methoden** vorgenommen werden, werden sofort wirksam. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

