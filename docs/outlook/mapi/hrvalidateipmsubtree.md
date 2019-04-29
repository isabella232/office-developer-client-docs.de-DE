---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436573"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt einem Nachrichtenspeicher standardmäßige zwischenmenschliche Nachrichten-Ordner hinzu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Parameter

 _lpMDB_
  
> in Zeiger auf das Nachrichtenspeicherobjekt, dem die Ordner hinzugefügt werden sollen. 
    
 _ulFlags_
  
> in Bitmaske der Flags, die verwendet werden, um zu steuern, wie die Ordner erstellt werden. Die folgenden Flags können festgelegt werden:
    
MAPI_FORCE_CREATE 
  
> Die Ordner sollten vor der Erstellung überprüft werden, auch wenn die Eigenschaften des Nachrichtenspeichers darauf hinweisen, dass Sie gültig sind. Eine Clientanwendung legt dieses Flag in der Regel fest, wenn ein Fehler darauf hinweist, dass die Struktur eines vorhandenen Ordners beschädigt wurde. 
    
MAPI_FULL_IPM_TREE 
  
> Der vollständige Satz von IPM-Ordnern sollte im Stammordner des Nachrichtenspeichers erstellt werden. Die Ordnertitel in der Hierarchie sind:
    
    - Ordneransichten
    
    - Allgemeine Ansichten
    
    - Such Stamm\*
    
    - IPM-unterStruktur\*
    
    - Posteingang
    
    - Postausgang
    
    - Gelöschte Elemente\*
    
    - Gesendete Elemente
    
    Dabei sind die drei mit \* gekennzeichneten Ordner der Mindestsatz, der auch dann erstellt wird, wenn das MAPI_FULL_IPM_TREE-Flag nicht festgelegt wurde. Eine Clientanwendung legt dieses Flag in der Regel fest, wenn der Nachrichtenspeicher, in dem die Ordner erstellt werden sollen, der Standardspeicher ist.
    
 _lpcValues_
  
> [in, out] Zeiger auf die Anzahl der [SPropValue](spropvalue.md) -Strukturen im Array, die im _lppProps_ -Parameter zurückgegeben werden. Der Wert des _lpcValues_ -Parameters kann NULL sein, wenn _lppProps_ NULL ist. 
    
 _lppProps_
  
> [in, out] Zeiger auf einen Zeiger auf ein Array von **SPropValue** -Strukturen, die Eigenschaftswerte für die **PR_VALID_FOLDER_MASK** ([pidtagvalidfoldermask (](pidtagvalidfoldermask-canonical-property.md))-Eigenschaft und die entsprechenden Eigenschaften für die Ordnereintrags-ID enthält. Wenn **HrValidateIPMSubtree** einen Posteingang im Nachrichtenspeicher erstellt, enthält das **SPropValue** -Array eine Posteingangs-ID mit einem speziellen Eigenschafts, das als `PROP_TAG(PT_BINARY, PROP_ID_NULL)`codiert ist. Der _lppProps_ -Parameter kann NULL sein, wodurch angegeben wird, dass für die aufrufende Implementierung kein **SPropValue** -Array zurückgegeben werden muss. 
    
 _lppMapiError_
  
> Out Zeiger auf einen Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur, die Versions-, Komponenten-und Kontextinformationen für einen Fehler enthält. Der Parameter _lppMAPIError_ wird auf NULL festgelegt, wenn keine **MAPIERROR** -Struktur zurückgegeben wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

MAPI verwendet die **HrValidateIPMSubtree** -Funktion intern, um die standardmäßige IPM-Unterstruktur in einem Nachrichtenspeicher zu erstellen, wenn der Informationsspeicher zum ersten Mal geöffnet wird oder wenn ein Speicher als Standardspeicher erstellt wird. Diese Funktion kann auch von Clientanwendungen verwendet werden, um Standardnachrichten Ordner zu überprüfen oder zu reparieren. 
  
 **HrValidateIPMSubtree** erstellt immer die Ordner Search root und IPM Subtree im Stammordner des Stores und im Ordner "Gelöschte Elemente" im Ordner "IPM subtree". Der IPM-subtree-Ordner ist der Stamm der IPM-Hierarchie in diesem Nachrichtenspeicher. Der Stammordner der Suche kann als Stamm einer Unterstruktur für Suchergebnisordner verwendet werden. 
  
IPM-Clients sollten ihre Ordneransicht beginnend beim Stammordner der IPM-Unterstruktur anzeigen und die darunter liegenden Ordner anzeigen. Informationen im Stammordner eines Nachrichtenspeichers sollten nicht auf der Benutzeroberfläche eines Clients angezeigt werden. Diese Funktion bedeutet, dass, wenn ein Clientinformationen ausblenden muss, die Informationen im Stammverzeichnis der IPM-Unterstruktur abgelegt werden können, wo es für den Benutzer nicht sichtbar ist. Im Gegensatz dazu können nicht-IPM-Anwendungen, die Nachrichten und Ordner für den Benutzer unsichtbar sein müssen, beispielsweise in einem Server basierten Nachrichtenspeicher, außerhalb der IPM-Hierarchie platziert werden. 
  
 **HrValidateIPMSubtree** legt die **PR_VALID_FOLDER_MASK** -Eigenschaft fest, um anzugeben, ob jeder erstellte IPM-Ordner eine gültige Eintrags-ID aufweist. Die folgenden Eigenschaften des Eintrags Identifiers des Nachrichtenspeichers werden auf die Eintragsbezeichner der entsprechenden Ordner festgelegt und im _lppProps_ -Parameter zusammen mit **PR_VALID_FOLDER_MASK**zurückgegeben: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([Pidtagcommonviewsentryid (](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([Pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([Pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([Pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([Pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([Pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([Pidtagviewsentryid (](pidtagviewsentryid-canonical-property.md))
  
> Ein Platzhalter- [PROP_TAG](prop_tag.md) für den IPM-Posteingang (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MstStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnValidateIPMSubtree  <br/> |MFCMAPI verwendet die **HrValidateIPMSubtree** -Methode, um einem Nachrichtenspeicher Standardordner hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

