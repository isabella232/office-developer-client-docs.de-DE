---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e198c46ffdc4a1bcc54f41149e68df7569edb702
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595945"
---
# <a name="itnefopentaggedbody"></a>ITnef::OpenTaggedBody

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet eine Datenstromschnittstelle für den Text einer gekapselten Nachricht.
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a>Parameter

 _lpMessage_
  
> [in] Ein Zeiger auf die Nachricht, der der Datenstrom zugeordnet ist. Diese Nachricht muss nicht die gleiche Nachricht sein, die im Aufruf der [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben wird. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie die Streamschnittstelle geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_CREATE 
  
> Wenn in der aktuellen Nachricht keine Eigenschaft vorhanden ist, sollte sie erstellt werden. Wenn die Eigenschaft vorhanden ist, sollten die aktuellen Daten in der Eigenschaft durch die Daten aus dem Transport-Neutral Encapsulation Format (TNEF)-Datenstrom ersetzt werden. Wenn eine Implementierung das MAPI_CREATE-Flag festlegt, sollte auch das MAPI_MODIFY-Flag festgelegt werden.
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Die Standardschnittstelle ist schreibgeschützt. MAPI_MODIFY müssen immer dann festgelegt werden, wenn MAPI_CREATE festgelegt ist.
    
 _lppStream_
  
> [out] Ein Zeiger auf einen Zeiger auf ein Streamobjekt, das den Text aus der **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) -Eigenschaft der übergebenen gekapselten Nachricht enthält und die [IStream-Schnittstelle](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) unterstützt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::OpenTaggedBody-Methode** auf, um eine Datenstromschnittstelle für den Text einer gekapselten Nachricht (d. h. für ein TNEF-Objekt) zu öffnen. 
  
Im Rahmen der Verarbeitung fügt **OpenTaggedBody** anlagentags ein oder analysiert diese, die die Position von Anlagen oder OLE-Objekten im Nachrichtentext angeben. Die Anlagentags haben das folgende Format: 
  
 **[[** _Anlagenname_ **:** _n_ im Namen **des** _Anlagencontainers_ **]]**
  
 _Der Anlagenname_ beschreibt das Anlagenobjekt.  _n_ ist eine Zahl, die die Anlage identifiziert, die Teil einer Sequenz ist, wobei der wert erhöht wird, der im  _lpKey-Parameter_ der [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion](opentnefstreamex.md) übergeben wird. und der Name des  _Anlagencontainers_ beschreibt die physische Komponente, in der sich das Anlagenobjekt befindet. 
  
 **OpenTaggedBody** liest Nachrichtentext aus und fügt ein Anlagentag überall dort ein, wo ein Anlagenobjekt ursprünglich im Text angezeigt wurde. Der ursprüngliche Nachrichtentext wird nicht geändert. 
  
Wenn eine Nachricht mit Tags an einen Datenstrom übergeben wird, werden die Tags entfernt, und die Anlagenobjekte werden an der Position der Tags im Datenstrom verschoben.
  
## <a name="see-also"></a>Siehe auch



[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[Kanonische PidTagBody-Eigenschaft](pidtagbody-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

