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
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428368"
---
# <a name="hierarchy-tables"></a>Hierarchietabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Hierarchietabelle enthält Informationen zu den Ordnern in einem Nachrichtenspeicher oder den Containern in einem Adressbuchcontainer. Jede Zeile einer Hierarchietabelle enthält eine Reihe von Spalten mit Informationen zu einem Ordner-oder Adressbuchcontainer. Hierarchietabellen werden in erster Linie von Clients verwendet und von Nachrichtenspeicher Anbietern implementiert, um eine Struktur von Ordnern und Unterordnern anzuzeigen und von Adressbuch Anbietern implementiert, um eine Struktur von Containern im Adressbuch anzuzeigen. Container, die keine Untercontainer enthalten können, wie durch das Fehlen des AB_SUBCONTAINERS-Flags in Ihrer **PR_CONTAINER_FLAGS** ([pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))-Eigenschaft angegeben, implementieren keine Hierarchietabelle.
  
Eine Hierarchietabelle kann durch Aufrufen aufgerufen werden:
  
- [IMAPIContainer:: GetHierarchy](imapicontainer-gethierarchytable.md).
    
    - Oder
    
- [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) übergibt **PR_CONTAINER_HIERARCHY** ([pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) als Property-Tag und IID_IMAPITable als Schnittstellenbezeichner.
    
Container und Ordner müssen beide Techniken zum Abrufen von Tabelleneigenschaften unterstützen. Es ist nicht akzeptabel, dass Dienstanbieter nur eine Möglichkeit zum Zugriff auf diese Tabellen unterstützen, da Clients erwarten, dass Sie die Wahl haben. 
  
> [!IMPORTANT]
> Speicheranbieter werden nicht unbedingt für die für Hierarchietabellen angegebenen Sortierreihenfolgen festgelegt. 
  
Der Aufruf von **IMAPIProp:: OpenProperty** beinhaltet den Zugriff auf die Hierarchietabelle durch Öffnen der zugehörigen Eigenschaft, **PR_CONTAINER_HIERARCHY**. Obwohl **PR_CONTAINER_HIERARCHY** nicht über die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode eines Ordners oder Containers abgerufen werden kann, wird es in das Property-Tag-Array aufgenommen, das von der [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode zurückgegeben wird. 
  
 **PR_CONTAINER_HIERARCHY** kann auch verwendet werden, um eine Hierarchietabelle aus einem Kopiervorgang einzubeziehen oder auszuschließen. Wenn ein Client **PR_CONTAINER_HIERARCHY** im *lpExcludeProps* -Parameter für [IMAPIProp:: CopyTo](imapiprop-copyto.md) in einem Kopiervorgang angibt, unterstützt der neue Ordner oder Container die Hierarchietabelle des ursprünglichen Ordners oder Containers nicht. 
  
Die folgenden Eigenschaften sind der erforderliche Spaltensatz in einer Hierarchietabelle:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([Pidtagdepth (](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([Pidtagstatus (](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** enthält den Namen für den Container oder Ordner, der in der Anzeige der Hierarchie angezeigt werden soll. 
  
 **PR_ENTRYID** ist die Eintrags-ID, die diesem Container oder Ordner zugeordnet ist. Es wird erwartet, dass es sich um eine langfristige Eintrags-ID handelt. Clients und MAPI können diese Eintrags-ID **** an OpenEntry weiterleiten, um den Container oder Ordner zu öffnen und den Inhalt durch Aufrufen von [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontentable anzuzeigen. 
  
 **PR_DEPTH** ist ein numerischer Wert, der die Einzugsebene für diesen Container oder Ordner angibt, wobei 0 (null) die oberste Ebene ist. Je tiefer in der Hierarchie sich ein Container oder Ordner befindet, desto höher ist der Wert für die **PR_DEPTH** -Eigenschaft. Clients verwenden die **PR_DEPTH** -Eigenschaft, um eine Hierarchietabelle entsprechend anzuzeigen, sodass Benutzer die Beziehungen zwischen über-und untergeordneten Elementen deutlich erkennen können. Die Container-oder Ordnertiefe ist immer relativ zum Container oder Ordner, der die Hierarchietabelle implementiert. 
  
 **PR_OBJECT_TYPE** ist immer auf MAPI_ABCONT für Adressbuch-Hierarchietabellen und MAPI_FOLDER für Ordner Hierarchietabellen festgelegt. 
  
 **PR_DISPLAY_TYPE** ist ein numerischer Wert, der angibt, wie ein Container oder Ordner in der Hierarchietabelle angezeigt wird. Sie wird hauptsächlich zu Anzeigezwecken verwendet, um visuell zwischen Container-oder Ordnertypen zu unterscheiden. Viele Nachrichtenspeicher-und Adressbuchanbieter verwenden Symbole für die verschiedenen Anzeigetypen. Der Anbieter muss diese Symbole bereitstellen. MAPI stellt keine Standardwerte bereit. 
  
MAPI definiert viele Werte für **PR_DISPLAY_TYPE**, einige, die für Ordner und andere gültig sind, die mit den Hierarchietabellen von Adressbuch Containern verwendet werden. In der Regel wird die **PR_DISPLAY_TYPE** eines Ordners auf DT_FOLDER festgelegt, um ein Standardordner Symbol anzugeben, DT_FOLDER_LINK, um ein Symbol anzugeben, das einen Link zu einem anderen Ordner darstellt, oder DT_FOLDER_SPECIAL, um ein anwendungsspezifisches Symbol anzugeben. DT_FOLDER_LINK wird mit Suchergebnis Ordnern verwendet. 
  
Zusätzlich zu diesen erforderlichen Spalten müssen Adressbuch-Hierarchietabellen die **PR_CONTAINER_FLAGS** -Eigenschaft enthalten. **PR_CONTAINER_FLAGS** gibt verschiedene Attribute zu einem Container in der Hierarchie an und wird verwendet, um einen Container von einem anderen zu unterscheiden. 
  
Eine optionale Eigenschaft für Adressbuch-Hierarchietabellen ist die **PR_AB_PROVIDER_ID** ([pidtagabproviderid (](pidtagabproviderid-canonical-property.md))-Eigenschaft.
  
Hierarchietabellen für Nachrichtenspeicher enthalten diese Eigenschaften in Ihrem erforderlichen Spaltensatz:
  
- **PR_FOLDER_TYPE** ([Pidtagfoldertype (](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([Pidtagsubfolders (](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([Pidtagcontentcount (](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([Pidtagcontentunreadcount (](pidtagcontentunreadcount-canonical-property.md))
    
Adressbuchanbieter müssen die folgenden **IMAPITable** -Methoden in ihren Hierarchietabellen Implementierungen unterstützen, da Sie für das integrierte MAPI-Adressbuch erforderlich sind: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::FindRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

