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
  
Öffnet eine Streamschnittstelle für den Text einer gekapselten Nachricht.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht, der der Datenstrom zugeordnet ist. Diese Nachricht muss nicht dieselbe Nachricht sein, die beim Aufruf der [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion übergeben](opentnefstreamex.md) wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Streamschnittstelle geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_CREATE 
  
> Wenn in der aktuellen Nachricht keine Eigenschaft vorhanden ist, sollte sie erstellt werden. Wenn die Eigenschaft vorhanden ist, sollten die aktuellen Daten in der Eigenschaft durch die Daten aus dem Transport-Neutral Encapsulation Format (TNEF)-Stream ersetzt werden. Wenn eine Implementierung das MAPI_CREATE legt, sollte sie auch das MAPI_MODIFY festlegen.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Die Standardschnittstelle ist schreibgeschützt. MAPI_MODIFY muss festgelegt werden, wenn MAPI_CREATE festgelegt wird.
    
 _lppStream_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Streamobjekt, das den Text aus der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))-Eigenschaft der übergebenen gekapselten Nachricht enthält und die [IStream-Schnittstelle](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) unterstützt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>Hinweise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::OpenTaggedBody-Methode** auf, um eine Streamschnittstelle für den Text einer gekapselten Nachricht (d. h. für ein TNEF-Objekt) zu öffnen. 
  
Im Rahmen der Verarbeitung fügt **OpenTaggedBody** Anlagentags ein oder analysiert sie, die die Position von Anlagen oder OLE-Objekten im Nachrichtentext angeben. Die Anlagentags haben das folgende Format: 
  
 **[[** _Anlagenname_ **:** _n_ **im** Namen des _Anlagencontainers_ **]]**
  
 _Anlagenname_ beschreibt das Attachment-Objekt.  _n_ ist eine Zahl, die die Anlage identifiziert, die Teil einer Sequenz ist, inkrementiert von dem Wert, der im  _lpKey-Parameter_ der [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben wird. und  _der Name des Anlagencontainers_ beschreibt die physische Komponente, in der sich das Anlageobjekt befindet. 
  
 **OpenTaggedBody** liest Nachrichtentext aus und fügt ein Anlagentag an jedem Ort ein, an dem ein Anlageobjekt ursprünglich im Text angezeigt wurde. Der ursprüngliche Nachrichtentext wird nicht geändert. 
  
Wenn eine Nachricht mit Tags an einen Datenstrom übergeben wird, werden die Tags entfernt, und die Anlagenobjekte werden an der Position der Tags im Datenstrom verschoben.
  
## <a name="see-also"></a>Siehe auch



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagBody (kanonische Eigenschaft)](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

