---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383742"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine Stream-Schnittstelle für den Text der Fehlermeldung der gekapselte.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht, die die Stream-Objekt zugeordnet sind. Diese Nachricht ist nicht erforderlich, um die gleiche Nachricht werden, die im Aufruf der Funktion [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder [OpenTnefStreamEx](opentnefstreamex.md) übergeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie die Schnittstelle Stream geöffnet ist. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_CREATE IST 
  
> Wenn eine Eigenschaft in der aktuellen Nachricht nicht vorhanden ist, sollte er erstellt werden. Wenn die Eigenschaft vorhanden ist, sollte die aktuellen Daten in der Eigenschaft mit den Daten aus dem Stream Transport-Neutral Encapsulation Format (TNEF) ersetzt werden. Wenn eine Implementierung der MAPI_CREATE ist Flag festlegt, sollte auch die Kennzeichen MAPI_MODIFY festgelegt.
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Die Standard-Schnittstelle ist schreibgeschützt. MAPI_MODIFY muss festgelegt werden, sobald MAPI_CREATE ist festgelegt wird.
    
 _lppStream_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Stream-Objekt, das den Text aus der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft des übergebenen enthält gekapselte Nachricht und, das die [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle unterstützt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Transport-Provider, Anbieter Nachricht und Gateways rufen Sie die **ITnef::OpenTaggedBody** -Methode zum Öffnen eine Stream-Schnittstelle für den Text der Fehlermeldung der gekapselte (d. h., eine TNEF-Objekts). 
  
Als Teil der Verarbeitung **OpenTaggedBody** eingefügt oder analysiert Anlage-Tags, die die Position des alle Anlagen oder OLE-Objekte in den Nachrichtentext angeben. Die Anlage-Tags sind im folgenden Format: 
  
 **[[** _Name der Anlage_ **:** _n_ **in** _Anlage Containernamen_ **]]**
  
 _Name der Anlage_ beschreibt das Attachment-Objekt.  _n_ ist eine Zahl, die die Anlage identifiziert, die Teil einer Sequenz ist von der im Parameter _LpKey_ der [OpenTNEFStream nicht ausgeführt werden](opentnefstream.md) oder der [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergebene Wert erhöht. und _Anlage Containername_ beschreibt die physikalische Komponente, in dem das Attachment-Objekt befindet. 
  
 **OpenTaggedBody** des Nachrichtentexts liest und einen Attachment-Tag eingefügt, unabhängig von dessen Speicherort ein Attachment-Objekt ursprünglich im Text angezeigt. Der Text der ursprünglichen Nachricht wird nicht geändert. 
  
Wenn eine Meldung mit Tags in einem Stream-Objekt übergeben wird, die Tags entfernt werden, und Attachment-Objekte werden in die Position der Tags im Stream-Objekt verschoben.
  
## <a name="see-also"></a>Siehe auch



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagBody (kanonische Eigenschaft)](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

