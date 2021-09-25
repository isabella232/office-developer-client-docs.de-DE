---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f344bcb32fea5ee651fa1d4b6c2430a005ed50f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575883"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt einen Zeiger auf eine Schnittstelle zurück, die für den Zugriff auf eine Eigenschaft verwendet werden kann.
  
```cpp
HRESULT OpenProperty(
  ULONG ulPropTag,
  LPCIID lpiid,
  ULONG ulInterfaceOptions,
  ULONG ulFlags,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _ulPropTag_
  
> [in] Das Eigenschaftstag für die Eigenschaft, auf die zugegriffen werden soll. Sowohl der Bezeichner als auch der Typ müssen im Eigenschaftentag enthalten sein.
    
 _lpiid_
  
> [in] Ein Zeiger auf den Bezeichner für die Schnittstelle, die für den Zugriff auf die Eigenschaft verwendet werden soll. Der  _lpiid-Parameter_ darf nicht **NULL** sein.
    
 _ulInterfaceOptions_
  
> [in] Daten, die sich auf die durch den  _lpiid-Parameter_ identifizierte Schnittstelle beziehen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Zugriff auf die Eigenschaft steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_CREATE 
  
> Wenn die Eigenschaft nicht vorhanden ist, sollte sie erstellt werden. Wenn die Eigenschaft vorhanden ist, sollte der aktuelle Wert der Eigenschaft verworfen werden. Wenn ein Aufrufer die MAPI_CREATE-Kennzeichnung festlegt, sollte auch das MAPI_MODIFY-Flag festgelegt werden.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenProperty** die erfolgreiche Rückgabe, möglicherweise bevor das Objekt für den Aufrufer vollständig verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann das Ausführen eines nachfolgenden Objektaufrufs einen Fehler auslösen. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY ist in folgenden Situationen erforderlich:
    
  - Beim Öffnen einer Streameigenschaft, z. **B. IID_IStream,** um sie zu ändern.
    
  - Beim Öffnen einer eingebetteten Nachrichtenanlage, z. [B. PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) mit **IID_IMessage** geöffnet, um sie zu ändern.
    
 _lppUnk_
  
> [out] Ein Zeiger auf die angeforderte Schnittstelle, die für den Eigenschaftenzugriff verwendet werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angeforderte Schnittstellenzeiger wurde erfolgreich zurückgegeben.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die angeforderte Schnittstelle wird für diese Eigenschaft nicht unterstützt.
    
MAPI_E_NO_ACCESS 
  
> Der Aufrufer verfügt über unzureichende Berechtigungen für den Zugriff auf die Eigenschaft.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt kann nicht über die angeforderte Schnittstelle auf diese Eigenschaft zugreifen.
    
MAPI_E_NOT_FOUND 
  
> Die angeforderte Eigenschaft ist nicht vorhanden, und MAPI_CREATE wurde nicht im  _ulFlags-Parameter_ festgelegt. 
    
MAPI_E_INVALID_PARAMETER 
  
> Der Eigenschaftstyp im Tag wird auf PT_UNSPECIFIED festgelegt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIProp::OpenProperty-Methode** ermöglicht den Zugriff auf eine Eigenschaft über eine bestimmte Schnittstelle. **OpenProperty** ist eine Alternative zu den Methoden [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps.](imapiprop-setprops.md) Wenn **getProps** oder **SetProps** einen Fehler verursacht, weil die Eigenschaft zu groß oder zu komplex ist, rufen Sie **OpenProperty** auf. **OpenProperty** wird in der Regel verwendet, um auf Eigenschaften des Typs PT_OBJECT zuzugreifen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

To access message attachments, open the **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) property with a different interface identifier, depending on the type of attachment. In der folgenden Tabelle wird beschrieben, wie **OpenProperty** für die verschiedenen Arten von Anlagen aufgerufen wird: 
  
|**Anlagetyp**|**Zu verwendende Schnittstellen-ID**|
|:-----|:-----|
|Binär  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Nachricht  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** ist eine Ableitung der [IStream-Schnittstelle,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) die auf einer OLE 2.0-Verbunddatei basiert. **IStreamDocfile** ist die beste Wahl für den Zugriff auf OLE 2.0-Anlagen, da dies den geringsten Aufwand erfordert. Sie können IID_IStreamDocFile für Eigenschaften verwenden, die Daten enthalten, die in strukturiertem Speicher gespeichert sind, die über die [IStorage-Schnittstelle](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) verfügbar sind. 
  
Weitere Informationen zur Verwendung von **OpenProperty** mit Anlagen finden Sie in der **PR_ATTACH_DATA_OBJ-Eigenschaft** und [beim Öffnen einer Anlage.](opening-an-attachment.md)
  
Verwenden Sie nicht den **IStream-Zeiger,** den Sie erhalten, um die [Seek-](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) oder [SetSize-Methode](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) aufzurufen, es sei denn, Sie verwenden eine Nullposition oder Größenvariable. Verlassen Sie sich außerdem nicht auf den Wert des  _plibNewPosition-Ausgabeparameters,_ der vom **Seek-Aufruf** zurückgegeben wird. 
  
Wenn Sie **OpenProperty** aufrufen, um auf eine Eigenschaft mit der **IStream-Schnittstelle** zuzugreifen, verwenden Sie nur diese Schnittstelle, um Änderungen daran vorzunehmen. Versuchen Sie nicht, die Eigenschaft mit einer der anderen [IMAPIProp : IUnknown-Methoden](imapipropiunknown.md) wie **SetProps** oder [IMAPIProp::D eleteProps](imapiprop-deleteprops.md)zu aktualisieren. 
  
Versuchen Sie nicht, eine Eigenschaft mit **OpenProperty** mehrmals zu öffnen. Die Ergebnisse sind nicht definiert, da sie von Anbieter zu Anbieter variieren können. 
  
Wenn Sie die zu öffnende Eigenschaft ändern müssen, legen Sie das flag MAPI_MODIFY fest. Wenn Sie nicht sicher sind, ob das Objekt die Eigenschaft unterstützt, sie jedoch für sinnvoll halten, legen Sie die Flags MAPI_CREATE und MAPI_MODIFY fest. Wenn MAPI_CREATE festgelegt wird, müssen auch MAPI_MODIFY festgelegt werden.
  
Sie sind dafür verantwortlich, den schnittstellenzeiger, der im  _lppUnk-Parameter_ zurückgegeben wird, in einen umgestalten, der für die im  _lpiid-Parameter_ angegebene Schnittstelle geeignet ist. Sie müssen auch den zurückgegebenen Zeiger verwenden, um die [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufzurufen, wenn Sie damit fertig sind. 
  
Manchmal reicht das Festlegen der Flags im  _ulFlags-Parameter_ nicht aus, um den Typ des Zugriffs auf die erforderliche Eigenschaft anzugeben. Sie können zusätzliche Daten, z. B. Flags, in den  _ulInterfaceOptions-Parameter_ einfügen. Diese Daten sind schnittstellenabhängig. Einige Schnittstellen (z. **B. IStream)** verwenden sie, andere dagegen nicht. Wenn Sie beispielsweise eine Eigenschaft öffnen, die mit **IStream** geändert werden soll, legen Sie zusätzlich zum MAPI_MODIFY das flag STGM_WRITE im  _UlInterfaceOptions-Parameter_ fest. Wenn Sie eine Tabelle mithilfe der [IMAPITable-Schnittstelle](imapitableiunknown.md) öffnen, können Sie  _ulInterfaceOptions_ auf MAPI_UNICODE festlegen, um anzugeben, ob die Spalten in der Tabelle, die Zeichenfolgeneigenschaften enthalten, im Unicode-Format vorliegen sollen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI verwendet die **IMAPIProp::OpenProperty-Methode,** um eine Streamschnittstelle für große Text- und binäre Eigenschaften abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)
- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
- [Öffnen einer Anlage](opening-an-attachment.md)

