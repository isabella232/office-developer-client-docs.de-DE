---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7f7c243995c633389ab8fa80a26dddd152347276
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565361"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält die Eigenschaftenbezeichner, die mindestens einen Eigenschaftennamen entsprechen.
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>Parameter

 _cPropNames_
  
> [in] Die Anzahl der Eigenschaftennamen, die auf den durch den Parameter _LppPropNames_ verwiesen. Wenn _LppPropNames_ NULL ist, muss der Parameter _cPropNames_ 0 sein. 
    
 _lppPropNames_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftennamen oder NULL. Bei Übergabe von NULL fordert Eigenschaftenbezeichner für alle Eigenschaftennamen in allen, die Eigenschaftensätze, die das Objekt Informationen verfügt. Der Parameter _LppPropNames_ darf nicht NULL sein, wenn das Flag MAPI_CREATE ist im _UlFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die angibt, wie die Eigenschaftenbezeichner zurückgegeben werden sollen. Das folgende Flag kann festgelegt werden:
    
MAPI_CREATE IST 
  
> Weist einen Eigenschaftenbezeichner an, wenn eine nicht noch, um eine oder mehrere der in der Array-Eigenschaft Name auf den _LppPropNames_enthaltenen Namen zugewiesen wurde. Dieses Kennzeichen registriert intern den Bezeichner in der Zuordnungstabelle Namensbezeichner-an.
    
 _lppPropTags_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Eigenschaftentags, vorhandene oder neu zugewiesenen Eigenschaftenbezeichner enthält. Die Eigenschaftentypen für die Eigenschaftentags in diesem Array werden auf **PT_UNSPECIFIED**festgelegt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Bezeichner für die angegebene Eigenschaftennamen wurden erfolgreich zurückgegeben.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine benannte Eigenschaften.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> War nicht genügend Arbeitsspeicher zum Abrufen der Bezeichner verfügbar.
    
MAPI_E_TOO_BIG 
  
> Der Vorgang kann nicht ausgeführt werden, da zu viele Eigenschaftentags zurückzugebenden erforderlich sind.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber eine oder mehrere Eigenschaftenbezeichner konnte nicht zurückgegeben werden. Der entsprechende Eigenschaftentyp für jede Eigenschaft nicht verfügbar ist **PT_ERROR** und des Bezeichners auf NULL gesetzt. Wenn diese Warnung zurückgegeben wird, bearbeiten Sie den Anruf als erfolgreich. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Finden Sie unter [Verwendung von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIProp::GetIDsFromNames** -Methode ruft ein Array von Eigenschaftentags, die die als Eigenschaftenbezeichner für eine oder mehrere benannte Eigenschaften enthalten. **IMAPIProp::GetIDsFromNames** kann aufgerufen werden, um Folgendes auszuführen: 
  
- Bezeichner für den neuen Namen erstellt.
    
- Rufen Sie IDs für bestimmte Namen ab.
    
- Abrufen von Bezeichnern für alle benannten Eigenschaften, die in das Objekt Zuordnung enthalten sind.
    
Benannte Eigenschaften werden in der Regel Zeichenfolgeneigenschaften Nachricht für Ordner und Nachrichten verwendet. Andere Objekte, wie messaging Profil Bereichen und Benutzer möglicherweise keine Unterstützung für die Zuordnung von Namen zu eigenschaftskennungen und zurückgeben MAPI_E_NO_SUPPORT vom **GetIDsFromNames**.
  
Ist ein Fehler, der einen Bezeichner für einen bestimmten Namen zurückgibt, **GetIDsFromNames** gibt MAPI_W_ERRORS_RETURNED zurück und legt den Eigenschaftstyp in der Eigenschaft Tag Array-Eintrag, der den Namen **PT_ERROR** und die ID 0 (null) entspricht. 
  
Namensbezeichner-Zuordnung wird durch ein Objekt **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md))-Eigenschaft dargestellt. **PR_MAPPING_SIGNATURE** enthält eine [MAPIUID](mapiuid.md) -Struktur, die den Dienstanbieter verantwortlich für das Objekt angibt. Wenn die **PR_MAPPING_SIGNATURE** -Eigenschaft für zwei Objekte übereinstimmt, wird davon ausgegangen Sie, dass diese Objekte die Namensbezeichner-Zuordnung verwenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Bezeichner, die Sie wieder in die Array-Tag-Eigenschaft auf das durch den Parameter _LppPropNames_ übergeben, muss im Bereich von 0 x 8000 zu 0xFFFE. Die Einträge in diesem Array müssen in der gleichen Reihenfolge die Namen übergebenen Arrays der Name-Eigenschaft mit _LppPropNames_gezeigt werden. 
  
Wenn Sie benannte Eigenschaften für einen Container unterstützen, verwenden Sie die Namensbezeichner-Zuordnung für alle Objekte in den Container (d. h., verwenden Sie keine andere Zuordnung für jeden Ordner in Ihrem Nachrichtenspeicher oder jede Nachricht im Ordner).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da die Eigenschaftentypen für die zurückgegebene Bezeichner in der Array-Tag-Eigenschaft auf den _LppPropTags_ auf **PT_UNSPECIFIED**festgelegt sind, müssen Sie rufen Sie die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um die genauen Typen abzurufen. 
  
Wenn Sie verschieben oder Objekte mit benannten Eigenschaften kopieren und die Quell- und Ziel-Objekte andere Zuordnung Signaturen, haben wie durch die Werte der Eigenschaften **PR_MAPPING_SIGNATURE** , müssen Sie die Namen während dieser Vorgänge beibehalten. Um Eigenschaftennamen beizubehalten, passen Sie die entsprechenden Eigenschaftenbezeichner entsprechend die Namensbezeichner-Zuordnung von Zielobjekt. 
  
Einige Objekte haben eine Obergrenze für die Anzahl der Eigenschaftenbezeichner, den, die Sie einen Namen eingeben können. Bewirkt ein Aufruf von **GetIDsFromNames** dieser Grenzwert überschritten wird, gibt die Methode MAPI_E_TOO_BIG zurück. In diesem Fall nach Bezeichnern abgefragt werden. 
  
Weitere Informationen finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::GetIDsFromNames** -Methode, um Eigenschaftentags für alle benannten Eigenschaften abzurufen, die zugeordnet wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Benannte Eigenschaften MAPI](mapi-named-properties.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

