---
title: IMAPIPropGetNamesFromIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetNamesFromIDs
api_type:
- COM
ms.assetid: 3efa4731-cf32-4a6c-9ba8-d059e58b0d98
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b968f76ee5b7f8b76b1ede9d8ce23b363c40e0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625560"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt die Eigenschaftennamen bereit, die einem oder mehreren Eigenschaftsbezeichnern entsprechen.
  
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
  
> [in, out] Bei der Eingabe ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält; andernfalls NULL, der angibt, dass alle Namen zurückgegeben werden sollen. Der **cValues-Member** für das Eigenschaftentagarray darf nicht 0 sein. Wenn  _lppPropTags_ ein gültiger Zeiger für die Eingabe ist, gibt **GetNamesFromIDs** Namen für jeden Eigenschaftsbezeichner zurück, der im Array enthalten ist. 
    
 _lpPropSetGuid_
  
> [in] Ein Zeiger auf eine GUID oder [GUID-Struktur,](guid.md) die einen Eigenschaftensatz identifiziert. Der  _parameter lpPropSetGuid_ kann auf einen gültigen Eigenschaftensatz verweisen oder NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Typ der zurückzugebenden Namen angibt. Die folgenden Flags können verwendet werden (wenn beide Flags festgelegt sind, werden keine Namen zurückgegeben):
    
MAPI_NO_IDS 
  
> Fordert an, dass nur Namen zurückgegeben werden, die als Unicode-Zeichenfolgen gespeichert sind. 
    
MAPI_NO_STRINGS 
  
> Fordert an, dass nur Namen zurückgegeben werden, die als numerische Bezeichner gespeichert sind. 
    
 _lpcPropNames_
  
> [out] Ein Zeiger auf die Anzahl der Eigenschaftennamenzeiger im Array, auf die der  _Parameter "lppPropNames"_ verweist. 
    
 _lpppPropNames_
  
> [out] Ein Zeiger auf ein Array von Zeigern auf [MAPINAMEID-Strukturen,](mapinameid.md) die Eigenschaftsnamen enthalten. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Eigenschaftennamen wurden erfolgreich zurückgegeben. 
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine benannten Eigenschaften. 
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, namen für eine oder mehrere Eigenschaften konnten jedoch nicht zurückgegeben werden. Die Eigenschaftentags für die fehlerhaften Eigenschaften weisen den Eigenschaftentyp **PT_ERROR** auf. Wenn diese Warnung zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden. Verwenden Sie das Makro **HR_FAILED, um** diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwenden von Makros für die Fehlerbehandlung.](using-macros-for-error-handling.md) 
    
MAPI_E_INVALID_PARAMETER 
  
> Das **cValues-Element** eines oder mehrerer Einträge im Eigenschaftentagarray, auf das durch  _lppPropTags_ verwiesen wird, ist auf 0 festgelegt. 
    
## <a name="remarks"></a>Bemerkungen

Während der Zugriff auf die meisten Eigenschaften über den Eigenschaftenbezeichner erfolgt, kann auf einige Eigenschaften über den Namen zugegriffen werden. Die **IMAPIProp::GetNamesFromIDs-Methode** kann aufgerufen werden, um Folgendes zu tun: 
  
- Dient zum Abrufen von Namen für bestimmte Eigenschaftsbezeichner in einem bestimmten Eigenschaftensatz.
    
- Dient zum Abrufen von Namen für bestimmte Eigenschaftsbezeichner in einem beliebigen Eigenschaftensatz.
    
- Ruft Namen für alle benannten Eigenschaften ab, die in der Zuordnung des Objekts enthalten sind.
    
Wenn  _lppPropTags_ auf ein gültiges Eigenschaftstagarray mit einem oder mehreren Eigenschaftsbezeichnern zeigt und  _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz zeigt, ignoriert **GetNamesFromIDs** den Eigenschaftensatz und die Eigenschaftstypen und gibt alle Namen zurück, die den angegebenen Bezeichnern zugeordnet sind. 
  
Wenn  _lppPropTags_ auf ein gültiges Eigenschaftstagarray mit einem oder mehreren Eigenschaftsbezeichnern zeigt und  _lpPropSetGuid_ NULL ist, gibt **GetNamesFromIDs** alle Namen zurück, die den angegebenen Bezeichnern zugeordnet sind. 
  
Wenn ein angegebener Bezeichner keinen Namen hat, gibt **GetNamesFromIDs** an der Stelle dieses Bezeichners in der in  _lpppPropNames zurückgegebenen_ Struktur NULL zurück und gibt auch MAPI_W_ERRORS_RETURNED zurück. 
  
Wenn  _sowohl lpPropSetGuid_ als  _auch lppPropTags_ NULL sind, weist **GetNamesFromIDs** ein neues Eigenschaftstagarray zu und gibt alle Namen für alle benannten Eigenschaften für das Objekt zurück. 
  
Wenn keine Namen zurückgegeben werden müssen, z. B. weil der angeforderte Eigenschaftensatz keine Eigenschaften enthält oder alle Eigenschaften einen Typ aufweisen, der von den Flags ausgeschlossen wird, führt **GetNamesFromIDs** folgende Aktionen aus: 
  
- Gibt S_OK zurück.
    
- Weist eine neue **SPropTagArray-Struktur** zu, wobei das **cValues-Element** auf 0 festgelegt wird. 
    
- Legt den Inhalt von  _lpcPropNames_ auf 0 fest. 
    
- Legt den Inhalt von  _lpppPropNames_ auf NULL fest. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn  _lpPropSetGuid_ auf einen gültigen Eigenschaftensatz zeigt und  _lppPropTags_ NULL ist, ist das Ergebnis nicht definiert. Sie können eine der folgenden Strategien verwenden: 
  
- Ignorieren Sie den Eigenschaftensatz, und geben Sie die Namen für die Bezeichner im Eigenschaftentagarray zurück.
    
- Geben Sie die Namen nur für die Bezeichner im Eigenschaftentagarray zurück, die zum angegebenen Eigenschaftensatz gehören.
    
- Fehler beim Aufruf und Zurückgeben MAPI_E_INVALID_PARAMETER. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um alle benannten Eigenschaften für ein Objekt abzurufen, müssen Sie zuerst die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) des Objekts aufrufen und dann die zurückgegebenen Bezeichner, die sich oberhalb des 0x8000-Bereichs befinden, an **GetNamesFromIDs** übergeben.
  
Wenn Sie einen gültigen Eigenschaftensatz, aber kein gültiges Eigenschaftstagarray übergeben, sollten Sie auf unvorhersehbare Ergebnisse vorbereitet sein. Einige Implementierungen von **GetNamesFromIDs** ignorieren den Eigenschaftensatz und geben die Namen für die Bezeichner im Eigenschaftentagarray zurück. Einige Implementierungen geben MAPI_E_INVALID_PARAMETER zurück. Andere Implementierungen geben weiterhin Namen für Bezeichner aller Eigenschaften im Eigenschaftensatz zurück. Wenn der Eigenschaftensatz PS_PUBLIC_STRINGS ist, kann **GetNamesFromIDs** alle Namen zurückgeben, die jemals erstellt wurden. Ob der Dienstanbieter eine Eigenschaft unter den Bezeichnern speichert, die den öffentlichen Zeichenfolgen zugeordnet sind, ist unwesentlich. 
  
Wenn Sie mit den Eigenschaftennamen fertig sind, überprüfen Sie den Inhalt des  _lpcPropNames-Parameters,_ um zu ermitteln, ob Namen zurückgegeben wurden. Wenn ja, rufen Sie die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) auf, um den Speicher freizugeben, auf den  _lppPropTags_ und  _lpppPropNames_ verweisen, wenn ein erfolgreiches Ergebnis zurückgegeben wird. Ein Aufruf von **MAPIFreeBuffer** reicht für jeden Parameter aus. Sie müssen das Array von Zeigern nicht durchlaufen und jede **MAPINAMEID-Struktur** einzeln freigeben. 
  
Weitere Informationen zu benannten Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI verwendet die **IMAPIProp::GetNamesFromIDs-Methode,** um benannte Eigenschaften nachzuschlagen, die zuvor zugeordnet wurden.  <br/> |
   
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

