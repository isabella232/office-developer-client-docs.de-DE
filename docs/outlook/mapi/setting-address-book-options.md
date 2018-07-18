---
title: Festlegen von Adressbuchoptionen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c64f84da6bece809176bf67985b6f55ce92414a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795512"
---
# <a name="setting-address-book-options"></a>Festlegen von Adressbuchoptionen

  
  
**Betrifft**: Outlook 
  
Sie können drei Eigenschaften festlegen, die Optionen für die Verwendung des Adressbuchs beschreiben:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    Die **PR_AB_SEARCH_PATH** -Eigenschaft wird von [IAddrBook::ResolveName](iaddrbook-resolvename.md) zum Bestimmen der Container werden im Zusammenhang mit Auflösung und die Reihenfolge, in der sie zugeordnet werden. Für jeden Container in **PR_AB_SEARCH_PATH**ruft **IAddrBook::ResolveName** seine [IABContainer](iabcontainer-resolvenames.md) -Methode. Container am Anfang des **PR_AB_SEARCH_PATH** sind vor dem Container am Ende des **PR_AB_SEARCH_PATH**durchsucht. 
    
    Die Reihenfolge der Suche in **PR_AB_SEARCH_PATH** wird angegeben, mithilfe der Struktur einer [SRowSet](srowset.md) , die dieselbe Struktur, die verwendet wird, um die Zeilen in einer Tabelle darstellen. Sie können den aktuellen Suchpfad durch Aufrufen der Methode [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) anzeigen und ändern, indem Sie die [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) -Methode aufrufen. 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    Die **PR_AB_DEFAULT_DIR** -Eigenschaft ist die Eintrags-ID der Adressbuchcontainer Anfangs angezeigt werden, wenn im Adressbuch angezeigt wird. Die Standardeinstellung Directory bleibt wirksam, bis Sie ihn ändern, indem Sie die [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode aufrufen. Sie können das Standardverzeichnis durch Aufrufen der Methode [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) anzeigen. 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Diese drei Eigenschaften sind spezielle, da Sie sie über die Standardmethoden **IMAPIProp** bearbeiten können. Stattdessen müssen Sie **IAddrBook** Methoden verwenden. Da keine dieser Eigenschaften mit **IMAPIProp::SetProps**geändert werden kann, ist es nicht erforderlich aufrufen, **IMAPIProp::SaveChanges** , damit Änderungen dauerhaft entfernt wird. Über die Methoden **IAddrBook** vorgenommenen Änderungen werden sofort wirksam. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

