---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 67c8540cf6901e3e077fd8fd269d155043b3c1ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561348"
---
# <a name="itneffinish"></a>ITnef::Finish

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beendet die Verarbeitung für alle Transport-Neutral Encapsulation Format (TNEF)-Vorgänge, die in die Warteschlange eingereiht sind und warten. 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpKey_
  
> [out] Ein Zeiger auf die **schlüsseleigenschaft PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) einer Anlage. Das TNEF-Kapselungsobjekt verwendet diesen Schlüssel, um eine Anlage mit ihrem Anlagenplatzierungstag in einer Nachricht zuzuordnen. Dieser Schlüssel sollte für jede Anlage eindeutig sein.
    
 _lpProblem_
  
> [out] Ein Zeiger auf einen Zeiger auf eine [zurückgegebene STnefProblemArray-Struktur.](stnefproblemarray.md) Die **STnefProblemArray-Struktur** gibt an, welche Eigenschaften ggf. nicht ordnungsgemäß codiert wurden. Wenn NULL im  _lpProblem-Parameter_ übergeben wird, wird kein Eigenschaftsproblemarray zurückgegeben. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf war erfolgreich und hat den erwarteten Wert oder die erwarteten Werte zurückgegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Transportanbieter, Nachrichtenspeicheranbieter und Gateways rufen die **ITnef::Finish-Methode** auf, um die Codierung aller Eigenschaften auszuführen, für die die Codierung in Aufrufen der Methoden [ITnef::AddProps](itnef-addprops.md) und [ITnef::SetProps](itnef-setprops.md) angefordert wurde. Wenn das TNEF-Objekt mit dem TNEF_ENCODE Flag für die [OpenTnefStream-](opentnefstream.md) oder [OpenTnefStreamEx-Funktion](opentnefstreamex.md) geöffnet wurde, codiert die **Finish-Methode** die angeforderten Eigenschaften in den Kapselungsstream, der an dieses Objekt übergeben wird. Wenn das TNEF-Objekt mit dem Flag TNEF_DECODE geöffnet wurde, decodiert die **Finish-Methode** die Eigenschaften aus dem TNEF-Stream und schreibt sie zurück in die Nachricht, zu der sie gehören. 
  
Nach dem **Finish-Aufruf** zeigt der Zeiger auf den Kapselungsstream auf das Ende der TNEF-Daten. Wenn der Anbieter oder das Gateway die TNEF-Streamdaten nach dem **Finish-Aufruf** verwenden muss, muss der Datenstromzeiger auf den Anfang der TNEF-Daten zurückgesetzt werden. 
  
Die TNEF-Implementierung meldet TNEF-Datenstromcodierungsprobleme, ohne den **Finish-Prozess zu** beenden. Die im _lpProblem-Parameter_ zurückgegebene [STnefProblemArray-Struktur](stnefproblemarray.md) gibt an, welche TNEF-Attribute oder MAPI-Eigenschaften ggf. nicht verarbeitet werden konnten. Der Wert, der im **Scode-Element** einer der in **STnefProblemArray enthaltenen STnefProblemArray-Strukturen** zurückgegeben wird, gibt das spezifische Problem an.  Der Anbieter oder das Gateway kann davon ausgehen, dass alle Eigenschaften oder Attribute, für die **Finish** keinen Problembericht zurückgibt, erfolgreich verarbeitet wurden. 
  
Wenn ein Anbieter oder Gateway nicht mit Problemarrays funktioniert, kann er NULL in  _lpProblem_ übergeben; in diesem Fall wird kein Problemarray zurückgegeben. 
  
Der in  _lpProblem_ zurückgegebene Wert ist nur gültig, wenn der Aufruf S_OK zurückgibt. Wenn S_OK zurückgegeben wird, sollte der Anbieter oder das Gateway die werte überprüfen, die in der **STnefProblemArray-Struktur** zurückgegeben werden. Wenn beim Anruf ein Fehler auftritt, wird die **STnefProblemArray-Struktur** nicht ausgefüllt, und der aufrufende Anbieter oder das Gateway sollte die Struktur nicht verwenden oder freigeben. Wenn beim Anruf kein Fehler auftritt, muss der aufrufende Anbieter oder das Gateway den Speicher für **STnefProblemArray** freigeben, indem er die [MAPIFreeBuffer-Funktion](mapifreebuffer.md) aufruft. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |SaveToTNEF  <br/> |MFCMAPI verwendet die **ITnef::Finish-Methode,** um die Verarbeitung des neuen TNEF-Streams abzuschließen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ITnef::AddProps](itnef-addprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[OpenTnefStream](opentnefstream.md)
  
[OpenTnefStreamEx](opentnefstreamex.md)
  
[PidTagAttachNumber (kanonische Eigenschaft)](pidtagattachnumber-canonical-property.md)
  
[STnefProblemArray](stnefproblemarray.md)
  
[ITnef : IUnknown](itnefiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

