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
  
> in Das Property-Tag für die Eigenschaft, auf die zugegriffen werden soll. Sowohl der Bezeichner als auch der Typ müssen im Property-Tag enthalten sein.
    
 _lpIID_
  
> in Ein Zeiger auf den Bezeichner für die Schnittstelle, die für den Zugriff auf die Eigenschaft verwendet werden soll. Der _lpIID_ -Parameter darf nicht **null**sein.
    
 _ulInterfaceOptions_
  
> in Daten, die sich auf die Schnittstelle beziehen, die durch den _lpIID_ -Parameter identifiziert wird. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Zugriff auf die Eigenschaft steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_CREATE 
  
> Wenn die Eigenschaft nicht vorhanden ist, sollte Sie erstellt werden. Wenn die Eigenschaft vorhanden ist, sollte der aktuelle Wert der Eigenschaft verworfen werden. Wenn ein Anrufer das MAPI_CREATE-Flag festlegt, sollte auch das MAPI_MODIFY-Flag festgelegt werden.
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** , dass OpenProperty erfolgreich zurückgegeben wird, möglicherweise bevor das Objekt vollständig für den Aufrufer verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler ausgelöst werden. 
    
MAPI_MODIFY 
  
> MAPI_MODIFY ist in diesen Situationen erforderlich:
    
  - Beim Öffnen einer Stream-Eigenschaft wie **IID_IStream**, um Sie zu ändern.
    
  - Beim Öffnen einer eingebetteten Nachrichtenanlage wie [PR_ATTACH_DATA_OBJ](pidtagattachdataobject-canonical-property.md) , die mit **IID_IMessage**geöffnet wurde, um Sie zu ändern.
    
 _lppUnk_
  
> Out Ein Zeiger auf die angeforderte Schnittstelle, die für den Eigenschaftenzugriff verwendet werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der angeforderte Schnittstellenzeiger wurde erfolgreich zurückgegeben.
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> Die angeforderte Schnittstelle wird für diese Eigenschaft nicht unterstützt.
    
MAPI_E_NO_ACCESS 
  
> Der Aufrufer verfügt nicht über ausreichende Berechtigungen für den Zugriff auf die Eigenschaft.
    
MAPI_E_NO_SUPPORT 
  
> Das Objekt kann nicht über die angeforderte Schnittstelle auf diese Eigenschaft zugreifen.
    
MAPI_E_NOT_FOUND 
  
> Die angeforderte Eigenschaft ist nicht vorhanden, und MAPI_CREATE wurde im _ulFlags_ -Parameter nicht festgelegt. 
    
MAPI_E_INVALID_PARAMETER 
  
> Der Eigenschaftentyp im-Tag ist auf PT_UNSPECIFIED festgelegt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIProp:: OpenProperty** -Methode ermöglicht den Zugriff auf eine Eigenschaft über eine bestimmte Schnittstelle. **OpenProperty** ist eine Alternative zu den [IMAPIProp::](imapiprop-getprops.md) GetProps-und [IMAPIProp::](imapiprop-setprops.md) setprope-Methoden. Wenn entweder **** GetProps oder SetProps fehlschlägt, weil die Eigenschaft zu umfangreich oder zu komplex ist, rufen Sie **OpenProperty**auf. **** **OpenProperty** wird normalerweise verwendet, um auf Eigenschaften vom Typ PT_OBJECT zuzugreifen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Um auf Nachrichtenanlagen zuzugreifen, öffnen Sie die **PR_ATTACH_DATA_OBJ** ([pidtagattachdataobject (](pidtagattachdataobject-canonical-property.md))-Eigenschaft mit einem anderen Schnittstellenbezeichner, je nach Art der Anlage. In der folgenden Tabelle wird beschrieben, **** wie Sie OpenProperty für die verschiedenen Typen von Anlagen aufrufen: 
  
|**Anlagentyp**|**Zu verwendende Schnittstellenkennung**|
|:-----|:-----|
|Binär  <br/> |IID_IStream  <br/> |
|Zeichenfolge  <br/> |IID_IStream  <br/> |
|Nachricht  <br/> |IID_IMessage  <br/> |
|OLE 2,0  <br/> |IID_IStreamDocfile  <br/> |
   
**IStreamDocfile** ist eine abLeitung der [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Schnittstelle, die auf einer OLE 2,0-Verbunddatei basiert. **IStreamDocfile** ist die beste Wahl für den Zugriff auf OLE 2,0-Anlagen, da dies den geringsten Aufwand erfordert. Sie können IID_IStreamDocFile für diese Eigenschaften verwenden, die in strukturiertem Speicher gespeicherte Daten enthalten, die über die [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) -Schnittstelle verfügbar sind. 
  
Weitere Informationen zur Verwendung von OpenProperty **** mit Anlagen finden Sie unter der **PR_ATTACH_DATA_OBJ** -Eigenschaft und [Öffnen einer Anlage](opening-an-attachment.md).
  
Verwenden Sie nicht den **IStream** -Zeiger, den Sie erhalten, um die [Seek](https://msdn.microsoft.com/library/aa380043%28v=VS.85%29.aspx) -oder SetSize-Methode aufzurufen, es sei denn, Sie verwenden eine NULL-oder größenvariable. [](https://msdn.microsoft.com/library/aa380044%28v=VS.85%29.aspx) Verlassen Sie sich auch nicht auf den Wert des _plibNewPosition_ -Ausgabeparameters, der vom **Seek** -Aufruf zurückgegeben wird. 
  
Wenn Sie **OpenProperty** aufrufen, um auf eine Eigenschaft mit der **IStream** -Schnittstelle zuzugreifen, verwenden Sie nur diese Schnittstelle, um Änderungen daran vorzunehmen. Versuchen Sie nicht, die Eigenschaft mit einer der anderen [IMAPIProp: IUnknown](imapipropiunknown.md) -Methoden wie SetProps **** oder [IMAPIProp::D eleteprops](imapiprop-deleteprops.md)zu aktualisieren. 
  
Versuchen Sie nicht, eine Eigenschaft mit **OpenProperty** mehrmals zu öffnen. Die Ergebnisse sind nicht definiert, da Sie von Anbieter zu Anbieter variieren können. 
  
Wenn Sie die zu öffnende Eigenschaft ändern müssen, legen Sie das MAPI_MODIFY-Flag fest. Wenn Sie nicht sicher sind, ob das Objekt die Eigenschaft unterstützt, aber Sie denken, dass dies der Fall sein sollte, legen Sie die MAPI_CREATE-und MAPI_MODIFY-Flags fest. Wenn MAPI_CREATE festgelegt ist, muss auch MAPI_MODIFY festgelegt werden.
  
Sie sind für die neuumwandlung des im _lppUnk_ -Parameter zurückgegebenen Schnittstellenzeigers in einen verantwortlich, der für die im _lpIID_ -Parameter angegebene Schnittstelle geeignet ist. Sie müssen auch den zurückgegebenen Zeiger verwenden, um seine [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methode aufzurufen, wenn Sie damit fertig sind. 
  
Manchmal genügt es nicht, die Flags im _ulFlags_ -Parameter festzulegen, um den Typ des erforderlichen Zugriffs auf die Eigenschaft anzugeben. Sie können zusätzliche Daten wie Flags in den Parameter _ulInterfaceOptions_ einfügen. Diese Daten sind Benutzeroberflächen abhängig. Einige Schnittstellen (wie **IStream**) verwenden Sie, andere nicht. Wenn Sie beispielsweise eine Eigenschaft öffnen, die mit **IStream**geändert werden soll, legen Sie zusätzlich zu MAPI_MODIFY das STGM_WRITE-Flag im _ulInterfaceOptions_ -Parameter fest. Wenn Sie eine Tabelle mithilfe der [IMAPITable](imapitableiunknown.md) -Schnittstelle öffnen, können Sie _ulInterfaceOptions_ auf MAPI_UNICODE festlegen, um anzugeben, ob die Spalten in der Tabelle, die Zeichenfolgeneigenschaften enthalten sollen, im Unicode-Format vorliegen sollen. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|StreamEditor. cpp  <br/> |CStreamEditor:: ReadTextStreamFromProperty  <br/> |MFCMAPI verwendet die **IMAPIProp:: OpenProperty** -Methode, um eine Stream-Schnittstelle für umfangreiche Text-und Binär Eigenschaften abzurufen.  <br/> |
   
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

