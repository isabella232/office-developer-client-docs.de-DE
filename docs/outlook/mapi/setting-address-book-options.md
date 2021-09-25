---
title: Festlegen von Adressbuchoptionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5b1cabe090b9cb34b86cee3690c71ca0173fd721
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624230"
---
# <a name="setting-address-book-options"></a>Festlegen von Adressbuchoptionen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können drei Eigenschaften festlegen, die Optionen für die Verwendung des Adressbuchs beschreiben:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    Die **PR_AB_SEARCH_PATH-Eigenschaft** wird von [IAddrBook::ResolveName](iaddrbook-resolvename.md) verwendet, um die Container zu bestimmen, die an der Namensauflösung beteiligt sein sollen, und die Reihenfolge, in der sie beteiligt sein sollen. Für jeden Container in **PR_AB_SEARCH_PATH** ruft **IAddrBook::ResolveName** die [IABContainer::ResolveNames-Methode](iabcontainer-resolvenames.md) auf. Container am Anfang **PR_AB_SEARCH_PATH** werden vor Containern am Ende **PR_AB_SEARCH_PATH** durchsucht. 
    
    Die Suchreihenfolge in **PR_AB_SEARCH_PATH** wird mithilfe einer [SRowSet-Struktur](srowset.md) angegeben, derselben Struktur, die zum Darstellen von Zeilen in einer Tabelle verwendet wird. Sie können den aktuellen Suchpfad anzeigen, indem Sie die [IAddrBook::GetSearchPath-Methode](iaddrbook-getsearchpath.md) aufrufen und ändern, indem Sie die [IAddrBook::SetSearchPath-Methode](iaddrbook-setsearchpath.md) aufrufen. 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    Die **PR_AB_DEFAULT_DIR-Eigenschaft** ist der Eintragsbezeichner des Adressbuchcontainers, der anfänglich angezeigt werden soll, wenn das Adressbuch angezeigt wird. Die Standardverzeichniseinstellung bleibt wirksam, bis Sie sie durch Aufrufen der [IAddrBook::SetDefaultDir-Methode](iaddrbook-setdefaultdir.md) ändern. Sie können das Standardverzeichnis anzeigen, indem Sie die [IAddrBook::GetDefaultDir-Methode](iaddrbook-getdefaultdir.md) aufrufen. 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Diese drei Eigenschaften sind besonders, da sie nicht mit den standardmäßigen **IMAPIProp-Methoden** verwendet werden können. Stattdessen müssen Sie **IAddrBook-Methoden** verwenden. Da keine dieser Eigenschaften mit **IMAPIProp::SetProps** geändert werden kann, ist es nicht erforderlich, **IMAPIProp::SaveChanges** aufzurufen, um Änderungen dauerhaft vorzunehmen. Änderungen, die über die **IAddrBook-Methoden** vorgenommen werden, werden sofort wirksam. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

