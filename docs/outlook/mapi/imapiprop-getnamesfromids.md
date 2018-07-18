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
ms.openlocfilehash: a2ec6def319b1f4686a61e9f97a936bfeba0d410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792285"
---
# <a name="imapipropgetnamesfromids"></a>IMAPIProp::GetNamesFromIDs

  
  
**Betrifft**: Outlook 
  
Enthält die Eigenschaftennamen, die einen oder mehrere Eigenschaftenbezeichner entsprechen.
  
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
  
> [in, out] Bei Eingabe einen Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags enthält. andernfalls NULL, was bedeutet, dass alle Namen zurückgegeben werden sollen. Das Element **cValues** Array der Tag-Eigenschaft kann nicht 0 sein. Wenn _LppPropTags_ einen gültigen Zeiger für die Eingabe ist, gibt **GetNamesFromIDs** Namen für jede Eigenschaft-ID in das Array aufgenommen. 
    
 _lpPropSetGuid_
  
> [in] Ein Zeiger auf eine GUID oder eine [GUID](guid.md) -Struktur, einen Eigenschaftensatz angibt. Der Parameter _LpPropSetGuid_ kann auf einen gültigen Eigenschaftensatz oder NULL sein. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des zurückzugebenden Namen angibt. Die folgenden Werte können verwendet werden (wenn beide Attribute festgelegt sind, keine Namen zurückgegeben):
    
MAPI_NO_IDS 
  
> Anforderungen, die nur als Unicode-Zeichenfolgen gespeicherte Namen zurückgegeben werden soll. 
    
MAPI_NO_STRINGS 
  
> Anforderungen, die nur als numerischen Bezeichner gespeicherte Namen zurückgegeben werden soll. 
    
 _lpcPropNames_
  
> [out] Ein Zeiger auf eine Anzahl von der Eigenschaft Name Zeigern im Array auf den durch den Parameter _LppPropNames_ verwiesen. 
    
 _lpppPropNames_
  
> [out] Ein Zeiger auf ein Array von Zeigern für [MAPINAMEID](mapinameid.md) Strukturen, Eigenschaftennamen enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Eigenschaftennamen wurden erfolgreich zurückgegeben. 
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt unterstützt keine benannte Eigenschaften. 
    
MAPI_W_ERRORS_RETURNED 
  
> Der Aufruf war insgesamt erfolgreich, aber Namen für eine oder mehrere Eigenschaften konnte nicht zurückgegeben werden. Die Eigenschaftentags für die fehlerhafte Eigenschaften haben einen Eigenschaftentyp des **PT_ERROR**. Wenn diese Warnung zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet. Verwenden Sie das Makro **HR_FAILED** , um für diese Warnung zu testen. Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md). 
    
MAPI_E_INVALID_PARAMETER 
  
> Das **cValues** -Element aus einem oder mehreren der Einträge in der Array-Tag-Eigenschaft auf den _LppPropTags_ ist auf 0 festgelegt. 
    
## <a name="remarks"></a>Bemerkungen

Während der Zugriff auf die meisten Eigenschaften vom Eigenschaftenbezeichner ist, können einige Eigenschaften namentlich zugegriffen werden. Die **IMAPIProp::GetNamesFromIDs** -Methode kann aufgerufen werden, um Folgendes auszuführen: 
  
- Namen für bestimmte Eigenschaftenbezeichner in einer bestimmten Eigenschaft abrufen.
    
- Namen für bestimmte Eigenschaftenbezeichner in einer Reihe Eigenschaft abrufen.
    
- Abrufen von Namen für alle benannten Eigenschaften, die in das Objekt Zuordnung enthalten sind.
    
Wenn _LppPropTags_ verweist auf eine gültige Eigenschaft Tag-Array mit mindestens einen Eigenschaftenbezeichner und _LpPropSetGuid_ verweist auf eine gültige Eigenschaft festlegen, ignoriert die Eigenschaft festgelegt und die Eigenschaftentypen und gibt die Namen aller **GetNamesFromIDs** die auf die angegebene Bezeichner zuordnen. 
  
Wenn _LppPropTags_ verweist auf eine gültige Eigenschaft Tag Array mit einem oder mehreren Eigenschaftenbezeichner und _LpPropSetGuid_ ist NULL, **GetNamesFromIDs** gibt alle Namen, die dem angegebenen Bezeichner zugeordnet sind. 
  
Wenn ein angegebenen Bezeichner keinen Namen, **GetNamesFromIDs** gibt NULL zurück, in diesem Bezeichner Stelle in der Struktur in _LpppPropNames_ zurückgegeben und gibt auch MAPI_W_ERRORS_RETURNED zurück. 
  
Wenn _LpPropSetGuid_ und _LppPropTags_ NULL sind, **GetNamesFromIDs** ordnet ein neues Eigenschaft Tag Array und gibt die Namen aller benannten Eigenschaften für das Objekt zurück. 
  
Wenn es keine Namen sind zurückgegeben werden soll, führt möglicherweise, weil keine Eigenschaften vorhanden, in dem angeforderten Eigenschaftensatz sind oder alle Eigenschaften eines Typs werden durch die Kennzeichen ausgeschlossen werden **GetNamesFromIDs** Folgendes aus: 
  
- Gibt S_OK zurück.
    
- Ordnet eine neue **SPropTagArray** -Struktur, wenn das Element **cValues** auf 0 festlegen. 
    
- Der Inhalt des _LpcPropNames_ festgelegt auf 0. 
    
- Legt den Inhalt der _LpppPropNames_ auf NULL fest. 
    
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wenn _LpPropSetGuid_ verweist auf einen gültigen Eigenschaftensatz und _LppPropTags_ NULL ist, ist das Ergebnis nicht definiert. Sie können eine der folgenden Strategien verwenden: 
  
- Ignorieren Sie die Eigenschaft festgelegt, und zurückgegeben Sie die Namen für den Bezeichner in Array der Tag-Eigenschaft.
    
- Die Namen für die nur die Bezeichner in der Tag Array-Eigenschaft, die zu dem angegebenen Eigenschaftensatz gehören zurück.
    
- Ein Fehler auf den Anruf MAPI_E_INVALID_PARAMETER zurückgeben. 
    
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um alle benannten Eigenschaften für ein Objekt abzurufen, müssen Sie zunächst das Objekt [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode aufrufen, und übergeben Sie den zurückgegebenen IDs, die über dem Bereich 0 x 8000 zu **GetNamesFromIDs**sind.
  
Wenn Sie eine gültige Eigenschaft fest, jedoch keine gültige Eigenschaft Tag-Array übergeben, bereiten Sie für zu unvorhersehbaren Ergebnissen führen. Einige Implementierungen von **GetNamesFromIDs** ignorieren die Eigenschaft festgelegt und die Namen für den Bezeichner in Array der Tag-Eigenschaft zurückgegeben. Einige Implementierungen zurückgeben MAPI_E_INVALID_PARAMETER. Implementierungen wird weiterhin Namen für die IDs aller Eigenschaften im Eigenschaftensatz zurück. Wenn der Eigenschaftensatz PS_PUBLIC_STRINGS ist, können **GetNamesFromIDs** alle Namen zurück, die jemals erstellt wurden. Es ist, ob der Dienstanbieter, eine Eigenschaft unter den IDs der öffentlichen Zeichenfolgen zugeordnet speichert irrelevant. 
  
Wenn Sie mit den Eigenschaftennamen fertig sind, überprüfen Sie den Inhalt des Parameters _LpcPropNames_ , um zu bestimmen, ob alle Namen zurückgegeben wurden. Wenn dies der Fall ist, auf die Aufruf der [MAPIFreeBuffer](mapifreebuffer.md) -Funktion, um den Arbeitsspeicher freizugeben _LppPropTags_ und _LpppPropNames_ soll, wenn ein erfolgreiches Ergebnis zurückgegeben wird. Durch Aufrufen von **MAPIFreeBuffer** ist ausreichend für jeden Parameter. Sie müssen nicht das Array von Zeigern zu durchlaufen und jede **MAPINAMEID** Struktur einzeln frei. 
  
Weitere Informationen zu benannten Eigenschaften finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedProps  <br/> |MFCMAPI (engl.) verwendet die **IMAPIProp::GetNamesFromIDs** -Methode zum Nachschlagen von benannten Eigenschaften, die zuvor zugeordnet wurden.  <br/> |
   
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

