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
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433584"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Eigenschaftenbezeichner zur Verfügung, die einem oder mehreren Eigenschaftsnamen entsprechen.
  
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
  
> [in] Die Anzahl der Eigenschaftsnamen, auf die der  _lppPropNames-Parameter_ verweist. Wenn  _lppPropNames_ NULL ist, muss  _der cPropNames-Parameter_ 0 sein. 
    
 _lppPropNames_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftennamen oder NULL. Übergeben von NULL-Anforderungen Eigenschaftenbezeichner für alle Eigenschaftsnamen in allen Eigenschaftensätzen, über die das Objekt Informationen enthält. Der  _lppPropNames-Parameter_ darf nicht NULL sein, wenn MAPI_CREATE im  _ulFlags-Parameter festgelegt_ ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die angibt, wie die Eigenschaftenbezeichner zurückgegeben werden sollen. Das folgende Flag kann festgelegt werden:
    
MAPI_CREATE 
  
> Weist einem oder mehreren Namen im Eigenschaftennamenarray, auf die von  _lppPropNames_ verwiesen wird, einen Eigenschaftsbezeichner zu, falls noch keiner zugewiesen wurde. Mit diesem Flag wird der Bezeichner intern in der Tabelle für die Zuordnung von Namen zu Bezeichnern registriert.
    
 _lppPropTags_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Eigenschaftstags, das vorhandene oder neu zugewiesene Eigenschaftenbezeichner enthält. Die Eigenschaftstypen für die Eigenschaftstags in diesem Array werden auf **PT_UNSPECIFIED.**
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Bezeichner für die angegebenen Eigenschaftsnamen wurden erfolgreich zurückgegeben.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine benannten Eigenschaften.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Es war nicht genügend Arbeitsspeicher verfügbar, um die Bezeichner abzurufen.
    
MAPI_E_TOO_BIG 
  
> Der Vorgang kann nicht ausgeführt werden, da zu viele Eigenschaftstags zurückgegeben werden müssen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber mindestens eine Eigenschafts-ID konnte nicht zurückgegeben werden. Der entsprechende Eigenschaftstyp für jede nicht verfügbare Eigenschaft wird auf **PT_ERROR** und dessen Bezeichner auf Null festgelegt. Wenn diese Warnung zurückgegeben wird, behandeln Sie den Anruf als erfolgreich. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere [Informationen finden Sie unter Using Macros for Error Handling](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::GetIDsFromNames-Methode** ruft ein Array von Eigenschaftstags ab, die die Eigenschaftenbezeichner für eine oder mehrere benannte Eigenschaften enthalten. **IMAPIProp::GetIDsFromNames** kann aufgerufen werden, um die folgenden Schritte zu tun: 
  
- Erstellen sie Bezeichner für neue Namen.
    
- Ruft Bezeichner für bestimmte Namen ab.
    
- Ruft Bezeichner für alle benannten Eigenschaften ab, die in der Zuordnung des Objekts enthalten sind.
    
Benannte Eigenschaften werden in der Regel von Nachrichtenspeicheranbietern für Ordner und Nachrichten verwendet. Andere Objekte, z. B. Messagingbenutzer und Profilabschnitte, unterstützen möglicherweise nicht die Zuordnung von Namen zu Eigenschaftenbezeichnern und geben möglicherweise MAPI_E_NO_SUPPORT von **GetIDsFromNames zurück.**
  
Wenn ein Fehler auftritt, der einen Bezeichner für einen bestimmten Namen zurückgibt, gibt **GetIDsFromNames** MAPI_W_ERRORS_RETURNED zurück und legt den Eigenschaftentyp im Eigenschaftentagarrayeintrag fest, der dem Namen **auf PT_ERROR** und dem Bezeichner auf Null entspricht. 
  
Die Zuordnung zwischen Namen und Bezeichnern wird durch die Eigenschaft **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) eines Objekts dargestellt. **PR_MAPPING_SIGNATURE** enthält eine [MAPIUID-Struktur,](mapiuid.md) die den für das Objekt zuständigen Dienstanbieter angibt. Wenn die **PR_MAPPING_SIGNATURE-Eigenschaft** für zwei Objekte identisch ist, gehen Sie davon aus, dass diese Objekte dieselbe Zuordnung von Name zu Bezeichner verwenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die bezeichner, die Sie im Eigenschaftentagarray übergeben, auf das der  _lppPropNames-Parameter_ verweist, müssen sich im Bereich 0x8000 0xFFFE befindet. Die Einträge in diesem Array müssen in der gleichen Reihenfolge wie die Namen sein, die im Eigenschaftennamenarray übergeben werden, auf das _von lppPropNames verwiesen wird._ 
  
Wenn Sie benannte Eigenschaften in einem Container unterstützen, verwenden Sie für alle Objekte im Container dieselbe Zuordnung von Name zu Bezeichner (d. h. verwenden Sie keine andere Zuordnung für jeden Ordner im Nachrichtenspeicher oder jede Nachricht in Ihrem Ordner).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da die Eigenschaftstypen für die zurückgegebenen Bezeichner im Eigenschaftentagarray, auf das  _von lppPropTags_ verwiesen wird, auf **PT_UNSPECIFIED** festgelegt sind, müssen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) aufrufen, um die genauen Typen abzurufen. 
  
Wenn Sie Objekte mit benannten Eigenschaften verschieben oder kopieren und die Quell- und Zielobjekte unterschiedliche Zuordnungssignaturen aufweisen, wie durch die Werte ihrer **PR_MAPPING_SIGNATURE-Eigenschaften** angegeben, müssen Sie die Namen während dieser Vorgänge beibehalten. Um Eigenschaftsnamen zu erhalten, passen Sie die entsprechenden Eigenschaftenbezeichner an die Zuordnung von Name zu Bezeichner des Zielobjekts an. 
  
Einige Objekte haben eine Beschränkung der Anzahl von Eigenschaftsbezeichnern, die sie benennen können. Wenn bei einem Aufruf **von GetIDsFromNames** dieser Grenzwert überschritten wird, gibt die Methode MAPI_E_TOO_BIG. In diesem Fall abfrage nach Bezeichner. 
  
Weitere Informationen finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI verwendet die **IMAPIProp::GetIDsFromNames-Methode, um Eigenschaftstags** für alle benannten Eigenschaften zu erhalten, die zugeordnet wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Benannte Eigenschaften MAPI](mapi-named-properties.md)
  
[Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

