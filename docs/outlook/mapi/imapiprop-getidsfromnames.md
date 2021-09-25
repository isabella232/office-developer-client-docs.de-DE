---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4f79e82c1ecbca9f006d60a2eb724fc5900a5d68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564141"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Eigenschaftsbezeichner bereit, die einem oder mehreren Eigenschaftennamen entsprechen.
  
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
  
> [in] Die Anzahl der Eigenschaftennamen, auf die der  _Parameter "lppPropNames"_ verweist. Wenn  _lppPropNames_ NULL ist, muss der  _cPropNames-Parameter_ 0 sein. 
    
 _lppPropNames_
  
> [in] Ein Zeiger auf ein Array von Eigenschaftsnamen oder NULL. Das Übergeben von NULL fordert Eigenschaftsbezeichner für alle Eigenschaftsnamen in allen Eigenschaftensätzen an, zu denen das Objekt Informationen enthält. Der  _lppPropNames-Parameter_ darf nicht NULL sein, wenn das MAPI_CREATE-Flag im  _ulFlags-Parameter_ festgelegt ist. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die angibt, wie die Eigenschaftsbezeichner zurückgegeben werden sollen. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_CREATE 
  
> Weist einem oder mehreren der Namen im Eigenschaftennamenarray, auf die durch  _lppPropNames_ verwiesen wird, einen Eigenschaftsbezeichner zu, sofern dieser noch nicht zugewiesen wurde. Mit diesem Flag wird der Bezeichner intern in der Zuordnungstabelle "Name-zu-Bezeichner" registriert.
    
 _lppPropTags_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Array von Eigenschaftentags, das vorhandene oder neu zugewiesene Eigenschaftsbezeichner enthält. Die Eigenschaftstypen für die Eigenschaftentags in diesem Array werden auf **PT_UNSPECIFIED** festgelegt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Bezeichner für die angegebenen Eigenschaftennamen wurden erfolgreich zurückgegeben.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine benannten Eigenschaften.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Zum Abrufen der Bezeichner war nicht genügend Arbeitsspeicher verfügbar.
    
MAPI_E_TOO_BIG 
  
> Der Vorgang kann nicht ausgeführt werden, da zu viele Eigenschaftstags zurückgegeben werden müssen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber mindestens ein Eigenschaftsbezeichner konnte nicht zurückgegeben werden. Der entsprechende Eigenschaftstyp für jede nicht verfügbare Eigenschaft ist auf **PT_ERROR** und dessen Bezeichner auf Null festgelegt. Wenn diese Warnung zurückgegeben wird, behandeln Sie den Aufruf als erfolgreich. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Informationen zur Fehlerbehandlung finden Sie unter [Verwenden von Makros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIProp::GetIDsFromNames-Methode** ruft ein Array von Eigenschaftentags ab, die die Eigenschaftsbezeichner für eine oder mehrere benannte Eigenschaften enthalten. **IMAPIProp::GetIDsFromNames** kann aufgerufen werden, um Folgendes zu tun: 
  
- Erstellen Sie Bezeichner für neue Namen.
    
- Dient zum Abrufen von Bezeichnern für bestimmte Namen.
    
- Dient zum Abrufen von Bezeichnern für alle benannten Eigenschaften, die in der Zuordnung des Objekts enthalten sind.
    
Benannte Eigenschaften werden in der Regel von Nachrichtenspeicheranbietern für Ordner und Nachrichten verwendet. Andere Objekte, z. B. Messagingbenutzer und Profilabschnitte, unterstützen möglicherweise die Zuordnung von Namen zu Eigenschaftenbezeichnern nicht und geben möglicherweise MAPI_E_NO_SUPPORT von **GetIDsFromNames** zurück.
  
Wenn ein Fehler auftritt, der einen Bezeichner für einen bestimmten Namen zurückgibt, gibt **GetIDsFromNames** MAPI_W_ERRORS_RETURNED zurück und legt den Eigenschaftstyp im Eigenschaftstag-Arrayeintrag fest, der dem Namen **PT_ERROR** und dem Bezeichner auf Null entspricht. 
  
Die Zuordnung von Namen zu Bezeichnern wird durch **die PR_MAPPING_SIGNATURE** -[PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) -Eigenschaft eines Objekts dargestellt. **PR_MAPPING_SIGNATURE** enthält eine [MAPIUID-Struktur,](mapiuid.md) die den für das Objekt verantwortlichen Dienstanbieter angibt. Wenn die **PR_MAPPING_SIGNATURE-Eigenschaft** für zwei Objekte identisch ist, wird davon ausgegangen, dass diese Objekte dieselbe Zuordnung von Name zu Bezeichner verwenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Bezeichner, die Sie im Eigenschaftentagarray übergeben, auf das der  _Parameter "lppPropNames"_ verweist, müssen sich im 0x8000 0xFFFE Bereich befinden. Die Einträge in diesem Array müssen in derselben Reihenfolge wie die Namen sein, die im Eigenschaftennamenarray übergeben werden, auf die durch  _lppPropNames_ verwiesen wird. 
  
Wenn Sie benannte Eigenschaften in einem Container unterstützen, verwenden Sie dieselbe Namens-zu-Bezeichner-Zuordnung für alle Objekte in Ihrem Container (verwenden Sie also keine andere Zuordnung für jeden Ordner in Ihrem Nachrichtenspeicher oder für jede Nachricht in Ihrem Ordner).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da die Eigenschaftstypen für die zurückgegebenen Bezeichner im Eigenschaftentagarray, auf die durch  _lppPropTags_ verwiesen wird, auf **PT_UNSPECIFIED** festgelegt sind, müssen Sie die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) aufrufen, um die genauen Typen abzurufen. 
  
Wenn Sie Objekte mit benannten Eigenschaften verschieben oder kopieren und die Quell- und Zielobjekte unterschiedliche Zuordnungssignaturen aufweisen, wie durch die Werte ihrer **PR_MAPPING_SIGNATURE** Eigenschaften angegeben, müssen Sie die Namen während dieser Vorgänge beibehalten. Um Eigenschaftsnamen beizubehalten, passen Sie die entsprechenden Eigenschaftsbezeichner so an, dass sie der Zuordnung von Namen zu Bezeichnern des Zielobjekts entsprechen. 
  
Einige Objekte haben einen Grenzwert für die Anzahl der Eigenschaftsbezeichner, die sie benennen können. Wenn ein Aufruf von **GetIDsFromNames** bewirkt, dass dieser Grenzwert überschritten wird, gibt die Methode MAPI_E_TOO_BIG zurück. Fragen Sie in diesem Fall nach Bezeichner ab. 
  
Weitere Informationen finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI verwendet die **IMAPIProp::GetIDsFromNames-Methode,** um Eigenschaftentags für alle benannten Eigenschaften abzurufen, die zugeordnet wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Benannte Eigenschaften MAPI](mapi-named-properties.md)
  
[Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

