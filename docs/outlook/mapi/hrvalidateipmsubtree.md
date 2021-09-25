---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 14801ca87ad3eccbd2e7eb0e074b5b047ab095d3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614052"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt einem Nachrichtenspeicher standardmäßige IPM-Ordner (Interpersonal Message) hinzu. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
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
  
> [in] Zeiger auf das Nachrichtenspeicherobjekt, dem die Ordner hinzugefügt werden sollen. 
    
 _ulFlags_
  
> [in] Bitmaske mit Flags, die zum Steuern der Erstellung der Ordner verwendet werden. Die folgenden Flags können festgelegt werden:
    
MAPI_FORCE_CREATE 
  
> Die Ordner sollten vor der Erstellung überprüft werden, auch wenn Nachrichtenspeichereigenschaften angeben, dass sie gültig sind. Eine Clientanwendung legt dieses Kennzeichen in der Regel fest, wenn ein Fehler darauf hinweist, dass die Struktur eines vorhandenen Ordners beschädigt wurde. 
    
MAPI_FULL_IPM_TREE 
  
> Der vollständige Satz von IPM-Ordnern sollte im Stammordner des Nachrichtenspeichers erstellt werden. Die Ordnertitel in der Hierarchie sind:
    
    - Ordneransichten
    
    - Allgemeine Ansichten
    
    - Suchstamm\*
    
    - IPM-Unterstruktur\*
    
    - Posteingang
    
    - Postausgang
    
    - Gelöschte Elemente\*
    
    - Gesendete Elemente
    
    wobei die drei \* markierten Ordner die Mindestmenge sind, die auch dann erstellt wird, wenn das MAPI_FULL_IPM_TREE-Flag nicht festgelegt wurde. Eine Clientanwendung legt dieses Kennzeichen in der Regel fest, wenn der Nachrichtenspeicher, in dem die Ordner erstellt werden sollen, der Standardspeicher ist.
    
 _lpcValues_
  
> [in, out] Zeiger auf die Anzahl der [SPropValue-Strukturen](spropvalue.md) im Array, das im  _lppProps-Parameter_ zurückgegeben wird. Der Wert des  _lpcValues-Parameters_ kann Null sein, wenn  _lppProps_ NULL ist. 
    
 _lppProps_
  
> [in, out] Zeiger auf einen Zeiger auf ein Array von **SPropValue-Strukturen,** die Eigenschaftswerte für die **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) -Eigenschaft und für die entsprechenden Eigenschaften des Ordnereintrags-Bezeichners enthält. Wenn **HrValidateIPMSubtree** einen Posteingang im Nachrichtenspeicher erstellt, enthält das **SPropValue-Array** einen Eingangsbezeichner für den Posteingang mit einem speziellen Eigenschaftstag, das als codiert  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` ist. Der  _lppProps-Parameter_ kann NULL sein, was bedeutet, dass für die aufrufende Implementierung kein **SPropValue-Array** zurückgegeben werden muss. 
    
 _lppMapiError_
  
> [out] Zeiger auf einen Zeiger auf eine [MAPIERROR-Struktur,](mapierror.md) die Versions-, Komponenten- und Kontextinformationen für einen Fehler enthält. Der  _lppMAPIError-Parameter_ wird auf NULL festgelegt, wenn keine **MAPIERROR-Struktur** zurückgegeben wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

DIE MAPI verwendet die **HrValidateIPMSubtree-Funktion** intern, um die standardmäßige IPM-Unterstruktur in einem Nachrichtenspeicher zu erstellen, wenn der Speicher zum ersten Mal geöffnet wird oder wenn ein Speicher als Standardspeicher festgelegt wird. Diese Funktion kann auch von Clientanwendungen zum Überprüfen oder Reparieren von Standardnachrichtenordnern verwendet werden. 
  
 **HrValidateIPMSubtree** erstellt immer die Ordner "Suchstamm" und "IPM-Unterstruktur" im Stammordner des Speichers und den Ordner "Gelöschte Elemente" im Ordner "IPM-Unterstruktur". Der Ordner "IPM-Unterstruktur" ist der Stamm der IPM-Hierarchie in diesem Nachrichtenspeicher. Der Suchstammordner kann als Stamm einer Unterstruktur für Suchergebnisordner verwendet werden. 
  
IPM-Clients sollten ihre Ordneransicht beginnend mit dem IPM-Unterstrukturstammordner und untergeordneten Ordnern darunter anzeigen. Informationen im Stammordner eines Nachrichtenspeichers sollten nicht auf der Benutzeroberfläche eines Clients angezeigt werden. Diese Funktionalität bedeutet, dass, wenn ein Client Informationen ausblenden muss, die Informationen im IPM-Unterstrukturstammverzeichnis abgelegt werden können, wo sie für den Benutzer nicht sichtbar sind. Im Gegensatz dazu können Nicht-IPM-Anwendungen, bei denen Nachrichten und Ordner für den Benutzer unsichtbar sein müssen, z. B. in einem serverbasierten Nachrichtenspeicher, außerhalb der IPM-Hierarchie platziert werden. 
  
 **HrValidateIPMSubtree** legt die **PR_VALID_FOLDER_MASK** Eigenschaft fest, um anzugeben, ob jeder von ihm erstellte IPM-Ordner einen gültigen Eintragsbezeichner aufweist. Die folgenden Eintragsbezeichnereigenschaften des Nachrichtenspeichers werden auf die Eintragsbezeichner der entsprechenden Ordner festgelegt und im  _Parameter "lppProps"_ zusammen mit **PR_VALID_FOLDER_MASK** zurückgegeben: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Ein Platzhalter [PROP_TAG](prop_tag.md) für den IPM-Posteingang (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI verwendet die **HrValidateIPMSubtree-Methode,** um einem Nachrichtenspeicher Standardordner hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

