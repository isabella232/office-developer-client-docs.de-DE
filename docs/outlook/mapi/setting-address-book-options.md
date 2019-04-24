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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351408"
---
# <a name="setting-address-book-options"></a>Festlegen von Adressbuchoptionen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Sie können drei Eigenschaften festlegen, die Optionen für die Verwendung des Adressbuchs beschreiben:
  
- **PR_AB_SEARCH_PATH** ([Pidtagabsearchpath (](pidtagabsearchpath-canonical-property.md))
    
    Die **PR_AB_SEARCH_PATH** -Eigenschaft wird von [IAddrBook::](iaddrbook-resolvename.md) ResolveName verwendet, um die an der Namensauflösung beteiligten Container und die Reihenfolge zu bestimmen, in der Sie beteiligt werden sollen. Für jeden Container in **PR_AB_SEARCH_PATH**ruft **IAddrBook::** ResolveName die [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) -Methode auf. Container am Anfang von **PR_AB_SEARCH_PATH** werden vor Containern am Ende von **PR_AB_SEARCH_PATH**durchsucht. 
    
    Die Suchreihenfolge in **PR_AB_SEARCH_PATH** wird mithilfe einer [SRowSet](srowset.md) -Struktur angegeben, der gleichen Struktur, die zum Darstellen von Zeilen in einer Tabelle verwendet wird. Sie können den aktuellen Suchpfad anzeigen, indem Sie die [IAddrBook:: GetSearchPath](iaddrbook-getsearchpath.md) -Methode aufrufen und Sie durch Aufrufen der [IAddrBook:: SetSearchPath](iaddrbook-setsearchpath.md) -Methode ändern. 
    
- **PR_AB_DEFAULT_DIR** ([Pidtagabdefaultdir (](pidtagabdefaultdir-canonical-property.md))
    
    Die **PR_AB_DEFAULT_DIR** -Eigenschaft ist der Eintragsbezeichner des Adressbuch Containers, der beim Anzeigen des Adressbuchs angezeigt werden soll. Die Standardverzeichnis Einstellung bleibt wirksam, bis Sie Sie ändern, indem Sie die [IAddrBook:: SetDefaultDir](iaddrbook-setdefaultdir.md) -Methode aufrufen. Sie können das Standardverzeichnis anzeigen, indem Sie die [IAddrBook:: GetDefaultDir](iaddrbook-getdefaultdir.md) -Methode aufrufen. 
    
- **PR_AB_DEFAULT_PAB** ([Pidtagabdefaultpab (](pidtagabdefaultpab-canonical-property.md))
    
Diese drei Eigenschaften sind etwas Besonderes, da Sie nicht mit den standardmäßigen **IMAPIProp** -Methoden arbeiten können. Stattdessen müssen Sie **IAddrBook** -Methoden verwenden. Da keine dieser Eigenschaften mit **IMAPIProp::** SetProps geändert werden kann, ist es nicht erforderlich, **IMAPIProp:: SaveChanges** aufzurufen, um Änderungen dauerhaft vorzunehmen. Änderungen, die über die **IAddrBook** -Methoden vorgenommen wurden, werden sofort wirksam. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

