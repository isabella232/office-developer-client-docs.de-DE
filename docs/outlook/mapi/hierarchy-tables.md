---
title: Hierarchietabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d135e0c224866cd2a675df2ef9ec1b206f3169ab
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580754"
---
# <a name="hierarchy-tables"></a>Hierarchietabellen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Eine Hierarchietabelle enthält Informationen zu den Ordnern in einem Nachrichtenspeicher oder in einer Adressbuchcontainer Container. Jede Zeile einer Hierarchie-Tabelle enthält eine Reihe von Spalten mit Informationen zu einem Ordner oder Adressbuchcontainer. Hierarchietabellen werden hauptsächlich von Clients verwendete und implementiert Zeichenfolgeneigenschaften Nachricht eine Struktur der Ordner und Unterordner anzeigt und implementiert mithilfe von adressbuchanbietern implementierte Struktur von Containern im Adressbuch angezeigt. Container, die Untercontainer, enthalten können nicht durch ohne das Flag AB_SUBCONTAINERS in ihrer **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))-Eigenschaft keine Hierarchietabelle zu implementieren.
  
Eine Hierarchietabelle kann durch Aufrufen von zugegriffen werden:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Oder -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) als Eigenschafts-Tag und IID_IMAPITable als Schnittstellenbezeichner übergeben.
    
Container und Ordner müssen beide Verfahren zum Abrufen von Eigenschaften der Tabelle unterstützen. Es ist nicht zulässig für Dienstanbieter unterstützen nur eine Möglichkeit, diese Tabellen zugegriffen werden, da Clients erwarten die Wahl. 
  
> [!IMPORTANT]
> Anbieter sind nicht unbedingt berücksichtigt die Sortierreihenfolge für Hierarchietabellen angegebenen festgelegt. 
  
Der Aufruf von **IMAPIProp::OpenProperty** umfasst das Zugreifen auf die Hierarchietabelle mithilfe die entsprechende Eigenschaft **PR_CONTAINER_HIERARCHY**öffnen. Obwohl **PR_CONTAINER_HIERARCHY** über einen Ordner oder für den Container [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden kann, ist es in Array der Tag-Eigenschaft enthalten, die von der [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode zurückgegeben wird. 
  
 **PR_CONTAINER_HIERARCHY** kann auch zum einschließen oder Ausschließen einer Hierarchietabelle einen Kopiervorgang verwendet werden. Wenn ein Client **PR_CONTAINER_HIERARCHY** im *LpExcludeProps* -Parameter für [IMAPIProp::CopyTo](imapiprop-copyto.md) in einen Kopiervorgang angibt, wird der neuen Ordner oder im Container nicht die Hierarchietabelle des ursprünglichen Ordner oder des Containers unterstützt. 
  
Die folgenden Eigenschaften bilden die erforderliche Spalte in einer Hierarchietabelle festgelegt:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** enthält den Namen für den Container oder Ordner, die in der Anzeige der Hierarchie angezeigt werden soll. 
  
 **PR_ENTRYID** ist die Eintrags-ID dieses Containers oder Ordner zugeordnet ist. Es wird erwartet, dass eine langfristige Eintrags-ID sein. Clients und MAPI können **OpenEntry** auf den Container oder Ordner öffnen und ihren Inhalt durch Aufrufen von [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)dieses Eintrags-ID übergeben. 
  
 **PR_DEPTH** ist ein numerischer Wert, der mit 0 (null) wird die oberste Ebene Einzugsebene für diesen Container oder Ordner angibt. Die tiefer in der Hierarchie einen Container oder Ordner befindet, je höher den Wert für die **PR_DEPTH** -Eigenschaft Clients verwenden die **PR_DEPTH** -Eigenschaft, um eine Hierarchietabelle entsprechend angezeigt, damit die Benutzer klar über- und untergeordnete Beziehungen sehen können. Container oder Ordner Tiefe ist immer relativ zu den Container oder Ordner die Hierarchietabelle implementieren. 
  
 **PR_OBJECT_TYPE** wird immer auf MAPI_ABCONT für Address Book Hierarchietabellen und MAPI_FOLDER für Ordner Hierarchietabellen festgelegt. 
  
 **PR_DISPLAY_TYPE** ist ein numerischer Wert, der beschreibt, wie eine Container oder einen Ordner in der Hierarchietabelle angezeigt wird. Es wird hauptsächlich für die Anzeige verwendet, zum Hervorheben zwischen verschiedenen Arten von Containern oder Ordner verwendet. Viele Nachricht speichern und address Book Anbieter Verwendung Symbole für die verschiedenen Anzeigetypen. Es ist bis zum Verwenden des Dienstanbieters für diese Symbole angeben. MAPI nicht Standardeinstellungen zur Verfügung. 
  
MAPI definiert viele Werte für **PR_DISPLAY_TYPE**, einige, die gelten für Ordner und andere Personen, die mit der Address Book Container der Hierarchietabellen verwendet werden. In der Regel ist einen Ordner **PR_DISPLAY_TYPE** auf DT_FOLDER festgelegt, um eine standardmäßige Ordnersymbol DT_FOLDER_LINK an, dass ein Symbol, das einen Link zu einem anderen Ordner darstellt, oder DT_FOLDER_SPECIAL an, dass ein Symbol, das anwendungsspezifische ist anzugeben. DT_FOLDER_LINK wird mit Suchergebnissen Ordner verwendet. 
  
Zusätzlich zu diesen erforderlichen Spalten müssen Address Book Hierarchietabellen die **PR_CONTAINER_FLAGS** -Eigenschaft enthalten. **PR_CONTAINER_FLAGS** gibt verschiedene Attribute über einem Container in der Hierarchie an und wird verwendet, um einen Container aus einer anderen unterscheiden. 
  
Eine optionale Eigenschaft für Address Book Hierarchietabellen ist **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Nachrichtenspeicher Hierarchietabellen fügen diese Eigenschaften in ihre erforderliche Spalte festlegen:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Von adressbuchanbietern implementierte müssen die folgenden Methoden **IMAPITable** in ihrer Hierarchie Tabelle Implementierungen unterstützen, da sie MAPI integrierte des Adressbuchs erforderlich sind: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

