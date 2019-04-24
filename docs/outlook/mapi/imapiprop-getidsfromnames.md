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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314840"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Eigenschaftenbezeichner bereit, die einem oder mehreren Eigenschaftsnamen entsprechen.
  
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
  
> in Die Anzahl der Eigenschaftennamen, auf die durch den _lppPropNames_ -Parameter verwiesen wird. Wenn _lppPropNames_ ist, muss der Parameter _cPropNames_ 0 sein. 
    
 _lppPropNames_
  
> in Ein Zeiger auf ein Array von Eigenschaftennamen oder NULL. Beim Übergeben von NULL werden Eigenschaftenbezeichner für alle Eigenschaftennamen in allen Eigenschaftensätzen angefordert, über die das Objektinformationen enthält. Der _lppPropNames_ -Parameter darf nicht NULL sein, wenn das MAPI_CREATE-Flag im _ulFlags_ -Parameter festgelegt ist. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die angibt, wie die Eigenschaftenbezeichner zurückgegeben werden sollen. Das folgende Flag kann festgelegt werden:
    
MAPI_CREATE 
  
> Weist einem oder mehreren Namen, die im Array der Eigenschaftennamen enthalten sind, auf die von _lppPropNames_verwiesen wurde, einen Eigenschaftenbezeichner zu, sofern noch keiner zugewiesen wurde. Dieses Flag registriert den Bezeichner intern in der Zuordnungstabelle Name-to-Identifier.
    
 _lppPropTags_
  
> Out Ein Zeiger auf einen Zeiger auf ein Array von Eigenschaftstags, das vorhandene oder neu zugewiesene Eigenschaftenbezeichner enthält. Die Eigenschaftentypen für die Eigenschaftstags in diesem Array sind auf **PT_UNSPECIFIED**festgelegt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Bezeichner für die angegebenen Eigenschaftennamen wurden erfolgreich zurückgegeben.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine benannten Eigenschaften.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Es war nicht genügend Arbeitsspeicher verfügbar, um die Bezeichner abzurufen.
    
MAPI_E_TOO_BIG 
  
> Der Vorgang kann nicht ausgeführt werden, da zu viele Eigenschaftentags zurückgegeben werden müssen.
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber ein oder mehrere Property Identifiers konnten nicht zurückgegeben werden. Der entsprechende Eigenschaftentyp für jede nicht verfügbare Eigenschaft wird auf **PT_ERROR** und dessen Bezeichner auf NULL festgelegt. Wenn diese Warnung zurückgegeben wird, behandeln Sie den Anruf als erfolgreich. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp:: GetIDsFromNames** -Methode ruft ein Array von Property-Tags ab, die die Eigenschaftenbezeichner für eine oder mehrere benannte Eigenschaften enthalten. **IMAPIProp:: GetIDsFromNames** kann aufgerufen werden, um folgende Aufgaben auszuführen: 
  
- Erstellen Sie Bezeichner für neue Namen.
    
- Abrufen von Bezeichnern für bestimmte Namen.
    
- Abrufen von Bezeichnern für alle benannten Eigenschaften, die in der Zuordnung des Objekts enthalten sind.
    
Benannte Eigenschaften werden in der Regel von Nachrichtenspeicher Anbietern für Ordner und Nachrichten verwendet. Andere Objekte, wie Messaging-Benutzer und Profilabschnitte, unterstützen möglicherweise nicht die Zuordnung von Namen zu Eigenschafts Bezeichnern und können MAPI_E_NO_SUPPORT von **GetIDsFromNames**zurückgeben.
  
Wenn ein Fehler auftritt, der einen Bezeichner für einen bestimmten Namen zurückgibt, gibt **GETIDSFROMNAMES** MAPI_W_ERRORS_RETURNED zurück und legt den Eigenschaftentyp im Array Eintrag für das Property-Tag fest, der dem Namen **PT_ERROR** und dem Bezeichner auf Null entspricht. 
  
Die Zuordnung von Namen zu Bezeichnern wird durch die **PR_MAPPING_SIGNATURE** ([pidtagmappingsignature (](pidtagmappingsignature-canonical-property.md))-Eigenschaft eines Objekts dargestellt. **PR_MAPPING_SIGNATURE** enthält eine [MAPIUID](mapiuid.md) -Struktur, die den für das Objektverantwortlichen Dienstanbieter angibt. Wenn die **PR_MAPPING_SIGNATURE** -Eigenschaft für zwei Objekte identisch ist, wird davon ausgegangen, dass diese Objekte dieselbe Name-zu-Bezeichner-Zuordnung verwenden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Bezeichner, die Sie zurückgeben, in das Eigenschaftentag-Array, auf das durch den _lppPropNames_ -Parameter verwiesen wird, müssen sich im 0X8000-0xFFFE-Bereich befinden. Die Einträge in diesem Array müssen in derselben Reihenfolge wie die Namen sein, die im Array der Eigenschaftennamen übergeben wurden, auf das durch _lppPropNames_verwiesen wird. 
  
Wenn Sie benannte Eigenschaften in einem Container unterstützen, verwenden Sie die gleiche Zuordnung Name-zu-Bezeichner für alle Objekte in Ihrem Container (das heißt, verwenden Sie keine andere Zuordnung für jeden Ordner in Ihrem Nachrichtenspeicher oder jede Nachricht in Ihrem Ordner).
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da die Eigenschaftentypen für die zurückgegebenen Bezeichner im Property-Tag-Array, auf das durch _lppPropTags_ verwiesen wird, auf **PT_UNSPECIFIED**festgelegt sind, müssen Sie die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode aufrufen, um die genauen Typen abzurufen. 
  
Wenn Sie Objekte mit benannten Eigenschaften verschieben oder kopieren und die Quell-und Zielobjekte unterschiedliche Zuordnungs Signaturen aufweisen, wie durch die Werte Ihrer **PR_MAPPING_SIGNATURE** -Eigenschaften angegeben, müssen Sie die Namen während dieser Vorgänge beibehalten. Um Eigenschaftsnamen beizubehalten, passen Sie die entsprechenden Eigenschaftenbezeichner so an, dass Sie der Name-to-Identifier-Zuordnung des Zielobjekts entsprechen. 
  
Einige Objekte haben einen Grenzwert für die Anzahl der Eigenschaftsbezeichner, die Sie benennen können. Wenn ein Aufruf von **GetIDsFromNames** bewirkt, dass dieser Grenzwert überschritten wird, gibt die Methode MAPI_E_TOO_BIG zurück. In diesem Fall Abfrage nach Bezeichner. 
  
Weitere Informationen finden Sie unter [MAPI-benannte Eigenschaften](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: FindAllNamedPropsUsed  <br/> |MFCMAPI verwendet die **IMAPIProp:: GetIDsFromNames** -Methode, um Eigenschaftentags für alle benannten Eigenschaften abzurufen, die zugeordnet wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Benannte Eigenschaften MAPI](mapi-named-properties.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

