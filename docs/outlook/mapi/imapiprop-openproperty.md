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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 656e5c5532edfc6c791ca30aa30f4c4d96847295
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792284"
---
# <a name="imapipropopenproperty"></a>IMAPIProp::OpenProperty

**Betrifft**: Outlook 
  
Gibt einen Zeiger auf eine Schnittstelle, die Zugriff auf eine Eigenschaft verwendet werden können.
  
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
  
> [in] Die Eigenschaftentag für die Eigenschaft zugegriffen werden. Der Bezeichner und der Typ müssen in das Eigenschafts-Tag enthalten sein.
    
 _lpiid_
  
> [in] Ein Zeiger auf den Bezeichner für die Schnittstelle für den Zugriff auf die Eigenschaft verwendet werden. Der Parameter _Lpiid_ darf nicht **null**sein.
    
 _ulInterfaceOptions_
  
> [in] Daten, die die Benutzeroberfläche, die vom Parameter _Lpiid_ beziehen. 
    
 _ulFlags_
  
> [in] Eine Bitmaske der Flags, die Steuerung des Zugriffs auf die Eigenschaft. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_CREATE IST 
  
> Wenn die Eigenschaft nicht vorhanden ist, sollte er erstellt werden. Wenn die Eigenschaft vorhanden ist, sollte der aktuelle Wert der Eigenschaft verworfen. Wenn ein Anrufer das Flag MAPI_CREATE ist festlegt, sollte auch die Kennzeichen MAPI_MODIFY festgelegt.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenProperty** erfolgreich, möglicherweise beendet, bevor das Objekt an den Anrufer vollständig verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann die nachfolgenden Objekt Anrufen ein Fehler ausgelöst. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY ist in den folgenden Situationen erforderlich:
    
  - Wenn eine Stream-Eigenschaft, wie beispielsweise **IID_IStream**zum Bearbeiten zu öffnen.
    
  - Wenn eine Anlage eingebettete Nachricht öffnen, wie [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) mit **IID_IMessage**zum Bearbeiten geöffnet.
    
 _lppUnk_
  
> [out] Ein Zeiger auf die angeforderte Schnittstelle für den Zugriff auf Eigenschaften verwendet werden soll.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der angeforderte Schnittstellenzeiger wurde erfolgreich zurückgegeben.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die angeforderte Schnittstelle wird für diese Eigenschaft nicht unterstützt.
    
MAPI_E_NO_ACCESS 
  
> Der Aufrufer verfügt nicht über ausreichende Berechtigungen zum Zugriff auf die Eigenschaft.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt kann nicht über Zugriff auf diese Eigenschaft über die angeforderte Schnittstelle bereit.
    
MAPI_E_NOT_FOUND 
  
> Die angeforderte-Eigenschaft ist nicht vorhanden und MAPI_CREATE ist in der _UlFlags_ -Parameter nicht festgelegt wurde. 
    
MAPI_E_INVALID_PARAMETER 
  
> Der Eigenschaftentyp im Tag wird auf PT_UNSPECIFIED festgelegt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIProp::OpenProperty** -Methode ermöglicht den Zugriff auf eine Eigenschaft über eine bestimmte Schnittstelle. **OpenProperty** ist eine Alternative an die Methoden [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPIProp::SetProps](imapiprop-setprops.md) . Rufen Sie **GetProps** oder **SetProps** fehlschlägt, weil die Eigenschaft zu groß oder zu komplex ist, **OpenProperty**. **OpenProperty** wird in der Regel vom Typ PT_OBJECT Eigenschaften zugreifen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Öffnen Sie den Zugriff auf e-Mail-Anlagen die **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))-Eigenschaft mit einem anderen Schnittstellenbezeichner, je nach Art der Anlage ein. In der folgenden Tabelle wird beschrieben, wie für die verschiedenen Typen von Anlagen **OpenProperty** aufrufen: 
  
|**Typ der Anlage**|**Schnittstellenbezeichner, der verwendet**|
|:-----|:-----|
|Binary  <br/> |IID_IStream  <br/> |
|String  <br/> |IID_IStream  <br/> |
|Nachricht  <br/> |IID_IMessage  <br/> |
|OLE 2.0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** ist eine Ableitung von der [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Schnittstelle, die auf eine Verbunddatei OLE 2.0 basiert. **IStreamDocfile** ist die beste Wahl für den Zugriff auf OLE 2.0-Anlagen, da er den geringsten Aufwand erfordert. Sie können IID_IStreamDocFile für diese Eigenschaften verwenden, die in strukturierten Speicher verfügbar über die Schnittstelle [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) gespeicherte Daten enthalten. 
  
Weitere Informationen zur Verwendung von **OpenProperty** mit Anlagen finden Sie unter der **PR_ATTACH_DATA_OBJ** -Eigenschaft und [eine Anlage zu öffnen](opening-an-attachment.md).
  
Verwenden Sie nicht den **IStream** Zeiger, den Sie erhalten, um entweder die [Seek](http://msdn.microsoft.com/en-us/library/aa380043%28v=VS.85%29.aspx) oder [SetSize](http://msdn.microsoft.com/en-us/library/aa380044%28v=VS.85%29.aspx) -Methode aufrufen, es sei denn, Sie eine NULL Variable Größe oder Position verwenden. Darüber hinaus verlassen Sie sich nicht auf dem Wert der _PlibNewPosition_ Output-Parameter des Aufrufs **Seek** . 
  
Wenn Sie **OpenProperty** Zugriff auf eine Eigenschaft mit der **IStream** -Schnittstelle aufrufen, verwenden Sie nur die Schnittstelle, es zu ändern. Versuchen Sie nicht so aktualisieren Sie die Eigenschaft mit den anderen [IMAPIProp: IUnknown](imapipropiunknown.md) Methoden, wie **SetProps** oder [IMAPIProp::DeleteProps](imapiprop-deleteprops.md). 
  
Versuchen Sie nicht mehr als einmal eine Eigenschaft mit **OpenProperty** geöffnet. Die Ergebnisse sind nicht definiert, da sie von Anbieter zu Anbieter unterschiedlich sein können. 
  
Wenn Sie so ändern Sie die Eigenschaft geöffnet werden soll müssen, legen Sie das MAPI_MODIFY-Flag. Wenn Sie nicht sicher sind, ob das Objekt die Eigenschaft unterstützt, aber es sollte Ihrer Meinung, legen Sie die Kennzeichen MAPI_CREATE ist und MAPI_MODIFY. Bei jedem MAPI_CREATE ist festgelegt ist, muss auch MAPI_MODIFY festgelegt werden.
  
Sie sind verantwortlich für recasting Zeiger der Schnittstelle, die für die Schnittstelle im _Lpiid_ -Parameter angegebene geeignet ist im Parameter _LppUnk_ zurückgegeben. Sie müssen außerdem den zurückgegebenen Zeiger verwenden, seine [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methode aufrufen, wenn Sie mit ihm fertig sind. 
  
In einigen Fällen festlegen die Kennzeichen in der _UlFlags_ -Parameter ist nicht genug sind, um den Zugriff auf die Eigenschaft anzugeben, der erforderlich ist. Sie können zusätzliche Daten enthält, wie Flags, die im Parameter _UlInterfaceOptions_ abgelegt. Diese Daten werden abhängige Schnittstelle. Einige Schnittstellen (wie **IStream**) verwenden, und andere nicht. Legen Sie die Kennzeichen STGM_WRITE im Parameter _UlInterfaceOptions_ neben MAPI_MODIFY beispielsweise beim Öffnen einer Eigenschaft mit **IStream**geändert werden soll. Beim Öffnen einer Tabelle mithilfe der [IMAPITable](imapitableiunknown.md) -Schnittstelle können Sie _UlInterfaceOptions_ festlegen, um Parameter MAPI_UNICODE, um anzugeben, ob die Spalten in der Tabelle, die Zeichenfolgeneigenschaften enthalten, im Unicode-Format sein soll. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|StreamEditor.cpp  <br/> |CStreamEditor::ReadTextStreamFromProperty  <br/> |MFCMAPI (engl.) wird die **IMAPIProp::OpenProperty** -Methode verwendet, um eine Stream-Schnittstelle für große Text- und binäre Eigenschaften abzurufen.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [HrIStorageFromStream](hristoragefromstream.md) 
- [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [IMAPIProp::SetProps](imapiprop-setprops.md)
- [IMAPISupport::IStorageFromStream](imapisupport-istoragefromstream.md)
- [IMAPITable: IUnknown](imapitableiunknown.md)
- [IMAPIProp: IUnknown](imapipropiunknown.md)
- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
- [Öffnen einer Anlage](opening-an-attachment.md)

