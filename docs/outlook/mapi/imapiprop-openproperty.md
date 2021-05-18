---
title: IMAPIPropOpenProperty
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.OpenProperty
api_type:
- COM
ms.assetid: e400e6cc-4e36-43fc-9304-b688a0a7fd77
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7bf1d6912e44319c36e288cd3870218e8c4e45ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319810"
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
  
> [in] Das Eigenschaftstag für die Eigenschaft, auf die zugegriffen werden soll. Sowohl der Bezeichner als auch der Typ müssen im Eigenschaftstag enthalten sein.
    
 _lpiid_
  
> [in] Ein Zeiger auf den Bezeichner für die Schnittstelle, die für den Zugriff auf die Eigenschaft verwendet werden soll. Der _lpiid-Parameter_ darf nicht null **sein.**
    
 _ulInterfaceOptions_
  
> [in] Daten, die sich auf die durch den  _lpiid-Parameter identifizierte Schnittstelle_ beziehen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Zugriff auf die Eigenschaft steuert. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_CREATE 
  
> Wenn die Eigenschaft nicht vorhanden ist, sollte sie erstellt werden. Wenn die Eigenschaft vorhanden ist, sollte der aktuelle Wert der Eigenschaft verworfen werden. Wenn ein Anrufer das MAPI_CREATE legt, sollte es auch das MAPI_MODIFY festlegen.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht die erfolgreiche Rückgabe von **OpenProperty,** möglicherweise bevor das Objekt vollständig für den Aufrufer verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY ist in folgenden Situationen erforderlich:
    
  - Beim Öffnen einer Streameigenschaft, **z. B. IID_IStream**, um sie zu ändern.
    
  - Wenn Sie eine eingebettete Nachrichtenanlage öffnen, z. [B.](pidtagattachdataobject-canonical-property.md) PR_ATTACH_DATA_OBJ mit IID_IMessage **,** um sie zu ändern.
    
 _lppUnk_
  
> [out] Ein Zeiger auf die angeforderte Schnittstelle, die für den Eigenschaftszugriff verwendet werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angeforderte Schnittstellenzeiger wurde erfolgreich zurückgegeben.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die angeforderte Schnittstelle wird für diese Eigenschaft nicht unterstützt.
    
MAPI_E_NO_ACCESS 
  
> Der Aufrufer verfügt über unzureichende Berechtigungen für den Zugriff auf die Eigenschaft.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt kann keinen Zugriff auf diese Eigenschaft über die angeforderte Schnittstelle bereitstellen.
    
MAPI_E_NOT_FOUND 
  
> Die angeforderte Eigenschaft ist nicht vorhanden, und MAPI_CREATE wurde nicht im  _ulFlags-Parameter_ festgelegt. 
    
MAPI_E_INVALID_PARAMETER 
  
> Der Eigenschaftentyp im Tag ist auf PT_UNSPECIFIED.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::OpenProperty-Methode** ermöglicht den Zugriff auf eine Eigenschaft über eine bestimmte Schnittstelle. **OpenProperty** ist eine Alternative zu den [Methoden IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps.](imapiprop-setprops.md) Wenn bei **GetProps oder** **SetProps** ein Fehler auftritt, da die Eigenschaft zu groß oder zu komplex ist, rufen Sie **OpenProperty auf.** **OpenProperty** wird in der Regel verwendet, um auf Eigenschaften vom Typ PT_OBJECT. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Öffnen Sie zum Zugreifen auf **Nachrichtenanlagen die PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) -Eigenschaft mit einem anderen Schnittstellenbezeichner, je nach Anlagetyp. In der folgenden Tabelle wird das Aufrufen **von OpenProperty für** die verschiedenen Anlagentypen beschrieben: 
  
|**Anlagetyp**|**Zu verwendende Schnittstellen-ID**|
|:-----|:-----|
|Binär  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Message  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** ist eine Ableitung der [IStream-Schnittstelle,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) die auf einer OLE 2.0-Verbunddatei basiert. **IStreamDocfile** ist die beste Wahl für den Zugriff auf OLE 2.0-Anlagen, da dies den geringsten Aufwand mit sich bringt. Sie können IID_IStreamDocFile eigenschaften verwenden, die Daten enthalten, die im strukturierten Speicher gespeichert sind, die über die [IStorage-Schnittstelle verfügbar](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) sind. 
  
Weitere Informationen zur Verwendung von **OpenProperty** mit Anlagen finden Sie unter **PR_ATTACH_DATA_OBJ-Eigenschaft** und [Öffnen einer Anlage](opening-an-attachment.md).
  
Verwenden Sie nicht den **IStream-Zeiger,** den Sie erhalten, um die [Seek-](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) oder [SetSize-Methode](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) auf aufruft, es sei denn, Sie verwenden eine Nullposition oder Größenvariable. Verlassen Sie sich außerdem nicht auf den Wert des  _plibNewPosition-Ausgabeparameters,_ der vom **Seek-Aufruf zurückgegeben** wird. 
  
Wenn Sie **OpenProperty aufrufen,** um auf eine Eigenschaft mit der **IStream-Schnittstelle** zu zugreifen, verwenden Sie nur diese Schnittstelle, um Änderungen daran vorzunehmen. Versuchen Sie nicht, die Eigenschaft mit einer der anderen [IMAPIProp : IUnknown-Methoden](imapipropiunknown.md) wie **SetProps** oder [IMAPIProp::D eleteProps](imapiprop-deleteprops.md)zu aktualisieren. 
  
Versuchen Sie nicht, eine Eigenschaft mit **OpenProperty mehr** als einmal zu öffnen. Die Ergebnisse sind nicht definiert, da sie von Anbieter zu Anbieter variieren können. 
  
Wenn Sie die zu öffnende Eigenschaft ändern müssen, legen Sie das Flag MAPI_MODIFY. Wenn Sie nicht sicher sind, ob das Objekt die Eigenschaft unterstützt, aber sie sollte, legen Sie die MAPI_CREATE- und MAPI_MODIFY fest. Wenn MAPI_CREATE festgelegt ist, muss MAPI_MODIFY festgelegt werden.
  
Sie sind für das Neucasting des im  _lppUnk-Parameter_ zurückgegebenen Schnittstellenzeigers auf einen für die im  _lpiid-Parameter_ angegebene Schnittstelle verantwortlich. Sie müssen auch den zurückgegebenen Zeiger verwenden, um die [IUnknown::Release-Methode auf](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufruft, wenn Sie damit fertig sind. 
  
Manchmal reicht das Festlegen der Flags im  _ulFlags-Parameter_ nicht aus, um den Typ des Zugriffs auf die erforderliche Eigenschaft anzugeben. Sie können zusätzliche Daten, z. B. Flags, im  _ulInterfaceOptions-Parameter_ speichern. Diese Daten sind schnittstellenabhängig. Einige Schnittstellen (z. **B. IStream)** verwenden sie, andere nicht. Wenn Sie beispielsweise eine Eigenschaft öffnen, die mit **IStream** geändert werden soll, legen Sie das STGM_WRITE-Flag im  _ulInterfaceOptions-Parameter_ zusätzlich zu MAPI_MODIFY. Wenn Sie eine Tabelle mithilfe der [IMAPITable-Schnittstelle](imapitableiunknown.md) öffnen, können Sie  _ulInterfaceOptions_ auf MAPI_UNICODE festlegen, um anzugeben, ob die Spalten in der Tabelle, die Zeichenfolgeneigenschaften enthalten, im Unicode-Format vorliegen sollen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI verwendet die **IMAPIProp::OpenProperty-Methode,** um eine Streamschnittstelle für große Text- und Binäreigenschaften abzurufen.  <br/> |
   
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

