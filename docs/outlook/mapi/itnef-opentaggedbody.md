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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348734"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine Stream-Schnittstelle für den Text einer gekapselte Nachricht.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> in Ein Zeiger auf die Nachricht, der der Stream zugeordnet ist. Diese Nachricht muss nicht dieselbe Nachricht sein, die beim Aufruf der [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergeben wird. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie die Stream-Schnittstelle geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_CREATE 
  
> Wenn eine Eigenschaft nicht in der aktuellen Nachricht vorhanden ist, sollte Sie erstellt werden. Wenn die Eigenschaft vorhanden ist, sollten die aktuellen Daten in der-Eigenschaft durch die Daten aus dem TNEF-Stream (Transport-Neutral Encapsulation Format) ersetzt werden. Wenn eine Implementierung das MAPI_CREATE-Flag festlegt, sollte auch das MAPI_MODIFY-Flag festgelegt werden.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Die Standardschnittstelle ist schreibgeschützt. MAPI_MODIFY muss festgelegt werden, wenn MAPI_CREATE festgelegt ist.
    
 _lppStream_
  
> Out Ein Zeiger auf einen Zeiger auf ein Stream-Objekt, das den Text aus der **PR_BODY** ([pidtagbody (](pidtagbody-canonical-property.md))-Eigenschaft der übergebenen verkapselten Nachricht enthält und die [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle unterstützt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.
    
## <a name="remarks"></a>Bemerkungen

Transport Anbieter, Nachrichtenspeicher Anbieter und Gateways rufen die **ITnef:: OpenTaggedBody** -Methode auf, um eine Stream-Schnittstelle für den Text einer gekapselte Nachricht zu öffnen (also für ein TNEF-Objekt). 
  
Im Rahmen seiner Verarbeitung fügt **OpenTaggedBody** entweder Anhänge-Tags ein, die die Position von Anlagen oder OLE-Objekten im Nachrichtentext Kennzeichen. Die Attachment-Tags haben das folgende Format: 
  
 **[[** _Attachment Name_ **:** _n_ **in** _Attachment Containername_ **]]**
  
 _Attachment Name_ Beschreibung des Attachment-Objekts;  _n_ ist eine Zahl, die die Anlage identifiziert, die Teil einer Sequenz ist, die von dem Wert inkrementiert wird, der im _lpKey_ -Parameter der [OpenTnefStream](opentnefstream.md) -oder [OpenTnefStreamEx](opentnefstreamex.md) -Funktion übergeben wird; und der _Name des Anlagen Containers_ beschreibt die physische Komponente, in der sich das Attachment-Objekt befindet. 
  
 **OpenTaggedBody** liest Nachrichtentext aus und fügt ein Attachment-Tag ein, wenn ein Attachment-Objekt ursprünglich im Text erschien. Der ursprüngliche Nachrichtentext wird nicht geändert. 
  
Wenn eine Nachricht mit Tags an einen Stream übergeben wird, werden die Tags entfernt, und die Attachment-Objekte werden an die Position der Tags im Stream verschoben.
  
## <a name="see-also"></a>Siehe auch



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Kanonische Pidtagbody (-Eigenschaft](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

