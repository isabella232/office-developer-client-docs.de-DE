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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f6688afde9b36a7722eaaf768f091481c15b7308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423573"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Eigenschaftsnamen zur Verfügung, die einem oder mehreren Eigenschaftsbezeichnern entsprechen.
  
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
  
> [in, out] Bei der Eingabe ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält. Andernfalls NULL, der angibt, dass alle Namen zurückgegeben werden sollen. Das **cValues-Element** für das Eigenschaftentagarray darf nicht 0 sein. Wenn  _lppPropTags_ ein gültiger Zeiger für die Eingabe ist, gibt **GetNamesFromIDs** Namen für jeden Eigenschaftenbezeichner zurück, der im Array enthalten ist. 
    
 _lpPropSetGuid_
  
> [in] Ein Zeiger auf eine GUID oder [GUID-Struktur,](guid.md) die einen Eigenschaftensatz identifiziert. Der  _lpPropSetGuid-Parameter_ kann auf einen gültigen Eigenschaftensatz oder NULL verweisen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückgibt. Die folgenden Flags können verwendet werden (wenn beide Flags festgelegt sind, werden keine Namen zurückgegeben):
    
MAPI_NO_IDS 
  
> Anforderungen, dass nur Als Unicode-Zeichenfolgen gespeicherte Namen zurückgegeben werden. 
    
MAPI_NO_STRINGS 
  
> Anforderungen, dass nur Namen zurückgegeben werden, die als numerische Bezeichner gespeichert sind. 
    
 _lpcPropNames_
  
> [out] Ein Zeiger auf eine Anzahl der Eigenschaftsnamenzeiger im Array, auf die der  _lppPropNames-Parameter_ verweist. 
    
 _lpppPropNames_
  
> [out] Ein Zeiger auf ein Array von Zeigern auf [MAPINAMEID-Strukturen,](mapinameid.md) die Eigenschaftsnamen enthalten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaftsnamen wurden erfolgreich zurückgegeben. 
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine benannten Eigenschaften. 
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, namen für eine oder mehrere Eigenschaften konnten jedoch nicht zurückgegeben werden. Die Eigenschaftstags für die fehlerhaften Eigenschaften haben den Eigenschaftentyp **PT_ERROR**. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich behandelt werden. Verwenden Sie zum Testen dieser Warnung das **HR_FAILED** Makro. Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> Das **cValues-Element** eines oder mehreren Einträgen im Eigenschaftentagarray, auf das  _von lppPropTags_ verwiesen wird, ist auf 0 festgelegt. 
    
## <a name="remarks"></a>Hinweise

Während der Zugriff auf die meisten Eigenschaften über den Eigenschaftenbezeichner festgelegt ist, kann auf einige Eigenschaften über den Namen zugegriffen werden. Die **IMAPIProp::GetNamesFromIDs-Methode** kann aufgerufen werden, um die folgenden Schritte zu tun: 
  
- Ruft Namen für bestimmte Eigenschaftenbezeichner in einem bestimmten Eigenschaftensatz ab.
    
- Rufen Sie Namen für bestimmte Eigenschaftenbezeichner in einem beliebigen Eigenschaftensatz ab.
    
- Ruft Namen für alle benannten Eigenschaften ab, die in der Zuordnung des Objekts enthalten sind.
    
Wenn  _lppPropTags_ auf ein gültiges Eigenschaftstagarray mit einem oder mehreren Eigenschaftsbezeichnern zeigt und  _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz verweist, ignoriert **GetNamesFromIDs** den Eigenschaftensatz und die Eigenschaftstypen und gibt alle Namen zurück, die den angegebenen Bezeichnern zuordnungen. 
  
Wenn  _lppPropTags_ auf ein gültiges Eigenschaftstagarray mit mindestens einem Eigenschaftsbezeichner verweist und  _lpPropSetGuid_ NULL ist, gibt **GetNamesFromIDs** alle Namen zurück, die den angegebenen Bezeichnern zuordnungen. 
  
Wenn ein angegebener Bezeichner keinen Namen hat, gibt **GetNamesFromIDs** NULL an der Stelle dieses Bezeichners in der Struktur zurück, die in  _lpppPropNames_ zurückgegeben wird, und gibt auch MAPI_W_ERRORS_RETURNED. 
  
Wenn  _lpPropSetGuid_ und  _lppPropTags_ NULL sind, weist **GetNamesFromIDs** ein neues Eigenschaftentagarray zu und gibt alle Namen für alle benannten Eigenschaften für das Objekt zurück. 
  
Wenn keine Namen zurückgegeben werden sollen, möglicherweise weil keine Eigenschaften im angeforderten Eigenschaftensatz enthalten sind oder alle Eigenschaften von einem Typ sind, der von den Flags ausgeschlossen wird, führt **GetNamesFromIDs** die folgenden Schritte aus: 
  
- Gibt S_OK.
    
- Weist eine neue **SPropTagArray-Struktur** zu, und das **cValues-Element** wird auf 0 festlegen. 
    
- Legt den Inhalt von  _lpcPropNames auf_ 0 fest. 
    
- Legt den Inhalt von  _lpppPropNames auf_ NULL fest. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn  _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz verweist und  _lppPropTags_ null ist, ist das Ergebnis nicht definiert. Sie können eine der folgenden Strategien verwenden: 
  
- Ignorieren Sie den Eigenschaftensatz, und geben Sie die Namen für die Bezeichner im Eigenschaftentagarray zurück.
    
- Geben Sie die Namen nur für die Bezeichner im Eigenschaftentagarray zurück, die zum angegebenen Eigenschaftensatz gehören.
    
- Führen Sie einen Fehler beim Anruf aus, und MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Zum Abrufen aller benannten Eigenschaften für ein Objekt müssen Sie zuerst die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) des Objekts aufrufen und dann die zurückgegebenen Bezeichner, die sich über dem 0x8000-Bereich befinden, an **GetNamesFromIDs übergeben.**
  
Wenn Sie einen gültigen Eigenschaftensatz, aber kein gültiges Eigenschaftstagarray übergeben, sollten Sie auf unvorhersehbare Ergebnisse vorbereitet sein. Einige Implementierungen von **GetNamesFromIDs** ignorieren den Eigenschaftensatz und geben die Namen für die Bezeichner im Eigenschaftentagarray zurück. Einige Implementierungen geben MAPI_E_INVALID_PARAMETER. Auch andere Implementierungen geben Namen für Bezeichner aller Eigenschaften im Eigenschaftensatz zurück. Wenn der Eigenschaftensatz PS_PUBLIC_STRINGS, **kann GetNamesFromIDs** alle Namen zurückgeben, die jemals erstellt wurden. Ob der Dienstanbieter eine Eigenschaft unter den den öffentlichen Zeichenfolgen zugeordneten Bezeichnern speichert, ist unerheblich. 
  
Wenn Sie mit den Eigenschaftennamen fertig sind, überprüfen Sie den Inhalt des  _lpcPropNames-Parameters,_ um zu ermitteln, ob Namen zurückgegeben wurden. Wenn ja, rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um den Arbeitsspeicher frei zu machen, auf den  _lppPropTags_ und  _lpppPropNames_ zeigen, wenn ein erfolgreiches Ergebnis zurückgegeben wird. Ein Aufruf von **MAPIFreeBuffer** ist für jeden Parameter ausreichend. Sie müssen nicht das Array von Zeigern durchlaufen und jede **MAPINAMEID-Struktur** einzeln frei geben. 
  
Weitere Informationen zu benannten Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI verwendet die **IMAPIProp::GetNamesFromIDs-Methode,** um benannte Eigenschaften nach zu suchen, die zuvor zugeordnet wurden.  <br/> |
   
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
  
[Verwenden von Makros für die Fehlerbehandlung](using-macros-for-error-handling.md)

