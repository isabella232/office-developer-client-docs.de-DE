---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329059"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Eigenschaftennamen bereit, die einem oder mehreren Eigenschafts Bezeichnern entsprechen.
  
```cpp
HRESULT GetNamesFromIDs(
  LPSPropTagArray FAR * lppPropTags,
  LPGUID lpPropSetGuid,
  ULONG ulFlags,
  ULONG FAR * lpcPropNames,
  LPMAPINAMEID FAR * FAR * lpppPropNames
);
```

## <a name="parameters"></a>Parameter

 _lppPropTags_
  
> [in, out] Bei der Eingabe ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält; andernfalls NULL, wodurch angegeben wird, dass alle Namen zurückgegeben werden sollen. Das **cValues** -Element für das Property-Tag-Array kann nicht 0 sein. Wenn _lppPropTags_ ein gültiger Zeiger auf der Eingabe ist, gibt **GetNamesFromIDs** die Namen der einzelnen Eigenschaftenbezeichner zurück, die im Array enthalten sind. 
    
 _lpPropSetGuid_
  
> in Ein Zeiger auf eine GUID oder eine [GUID](guid.md) -Struktur, die einen Eigenschaftensatz identifiziert. Der _lpPropSetGuid_ -Parameter kann auf einen gültigen Eigenschaftensatz verweisen oder NULL sein. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Typ der zurückzugebenden Namen angibt. Die folgenden Flags können verwendet werden (wenn beide Flags festgelegt sind, werden keine Namen zurückgegeben):
    
MAPI_NO_IDS 
  
> Fordert an, dass nur als Unicode-Zeichenfolgen gespeicherte Namen zurückgegeben werden. 
    
MAPI_NO_STRINGS 
  
> Fordert an, dass nur als numerische Bezeichner gespeicherte Namen zurückgegeben werden. 
    
 _lpcPropNames_
  
> Out Ein Zeiger auf die Anzahl der Eigenschaftennamen Zeiger im Array, auf das durch den _lppPropNames_ -Parameter verwiesen wird. 
    
 _lpppPropNames_
  
> Out Ein Zeiger auf ein Array von Zeigern auf [MAPINAMEID](mapinameid.md) -Strukturen, die Eigenschaftsnamen enthalten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaftennamen wurden erfolgreich zurückgegeben. 
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine benannten Eigenschaften. 
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber Namen für eine oder mehrere Eigenschaften konnten nicht zurückgegeben werden. Die Eigenschaftstags für die fehlerhaften Eigenschaften haben den Eigenschaftentyp **PT_ERROR**. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** -Makro. Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> Das **cValues** -Element eines oder mehrerer der Einträge im Array der Eigenschaftentags, auf die von _lppPropTags_ verwiesen wird, ist auf 0 festgelegt. 
    
## <a name="remarks"></a>Bemerkungen

Während der Zugriff auf die meisten Eigenschaften durch die Eigenschaftskennung erfolgt, können auf einige Eigenschaften über den Namen zugegriffen werden. Die **IMAPIProp:: GetNamesFromIDs** -Methode kann aufgerufen werden, um folgende Aufgaben auszuführen: 
  
- Ruft Namen für bestimmte Eigenschaftenbezeichner in einem bestimmten Eigenschaftensatz ab.
    
- Ruft Namen für bestimmte Eigenschaftenbezeichner in einem beliebigen Eigenschaftensatz ab.
    
- Ruft Namen für alle benannten Eigenschaften ab, die in der Zuordnung des Objekts enthalten sind.
    
Wenn _lppPropTags_ auf ein gültiges Property-Tag-Array mit einem oder mehreren Property Identifiers zeigt und _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz zeigt, ignoriert **GetNamesFromIDs** den Eigenschaftensatz und die Eigenschaftentypen und gibt alle Namen zurück. , die den angegebenen Bezeichnern zugeordnet sind. 
  
Wenn _lppPropTags_ auf ein gültiges Property-Tag-Array mit einem oder mehreren Property Identifiers zeigt und _LPPROPSETGUID_ den Wert NULL hat, gibt **GetNamesFromIDs** alle Namen zurück, die den angegebenen Bezeichnern zugeordnet sind. 
  
Wenn ein angegebener Bezeichner keinen Namen hat, gibt **GetNamesFromIDs** in der in _lpppPropNames_ zurückgegebenen Struktur NULL an der Stelle des Bezeichners zurück und gibt auch MAPI_W_ERRORS_RETURNED zurück. 
  
Wenn sowohl _lpPropSetGuid_ als auch _lppPropTags_ NULL sind, weist **GetNamesFromIDs** ein neues Property-Tag-Array zu und gibt alle Namen für alle benannten Eigenschaften für das Objekt zurück. 
  
Wenn keine Namen zurückgegeben werden sollen, möglicherweise, da keine Eigenschaften im angeforderten Eigenschaftensatz vorhanden sind oder alle Eigenschaften einen Typ aufweisen, der durch die Flags ausgeschlossen ist, führt **GetNamesFromIDs** Folgendes aus: 
  
- Gibt S_OK zurück.
    
- Weist eine neue **SPropTagArray** -Struktur zu, wobei das **cValues** -Element auf 0 festgelegt wird. 
    
- Legt den Inhalt von _lpcPropNames_ auf 0 fest. 
    
- Legt den Inhalt von _lpppPropNames_ auf NULL fest. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz verweist und _LPPPROPTAGS_ den Wert NULL hat, ist das Ergebnis nicht definiert. Sie können eine der folgenden Strategien verwenden: 
  
- Ignorieren Sie den Eigenschaftensatz, und geben Sie die Namen der Bezeichner im Property-Tag-Array zurück.
    
- Gibt die Namen nur für die Bezeichner im Property-Tag-Array zurück, die zum angegebenen Eigenschaftensatz gehören.
    
- Fehlschlagen des Anrufs, zurückgeben von MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie alle benannten Eigenschaften für ein Objekt abrufen möchten, müssen Sie zuerst die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode des Objekts aufrufen und dann die zurückgegebenen Bezeichner über dem 0X8000-Range an **GetNamesFromIDs**.
  
Wenn Sie einen gültigen Eigenschaftensatz, aber keinen gültigen Property-Tag-Array, werden auf unvorhersehbare Ergebnisse vorbereitet. Bei einigen Implementierungen von **GetNamesFromIDs** wird der Eigenschaftensatz ignoriert und die Namen der Bezeichner im Property-Tag-Array zurückgegeben. Einige Implementierungen geben MAPI_E_INVALID_PARAMETER zurück. Weitere Implementierungen geben Namen für Bezeichner aller Eigenschaften im Eigenschaftensatz zurück. Wenn der Eigenschaftensatz PS_PUBLIC_STRINGS ist, kann **GetNamesFromIDs** alle Namen zurückgeben, die jemals erstellt wurden. Ob der Dienstanbieter eine Eigenschaft unter den mit den öffentlichen Zeichenfolgen verknüpften Bezeichnern speichert, ist unerheblich. 
  
Wenn Sie die Eigenschaftennamen beendet haben, überprüfen Sie den Inhalt des _lpcPropNames_ -Parameters, um zu bestimmen, ob Namen zurückgegeben wurden. Wenn dies der Fall ist, rufen Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion auf, um den Arbeitsspeicher freizugeben, auf den von _lppPropTags_ und _lpppPropNames_ verwiesen wird, wenn ein erfolgreiches Ergebnis zurückgegeben wird. Ein Aufruf von **mapifreebufferfreigegeben** ist für jeden Parameter ausreichend; Sie müssen nicht das Array von Zeigern durchlaufen und jede **MAPINAMEID** -Struktur einzeln freigeben. 
  
Weitere Informationen zu benannten Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: FindAllNamedProps  <br/> |MFCMAPI verwendet die **IMAPIProp:: GetNamesFromIDs** -Methode, um benannte Eigenschaften nachzuschlagen, die zuvor zugeordnet wurden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)
  
[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPINAMEID](mapinameid.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[Benannte Eigenschaften MAPI](mapi-named-properties.md)
  
[Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md)

