---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a9aa6deeca930da82db61ba517796bfbc0676467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791900"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Betrifft**: Outlook 
  
Erstellt einen Eintrag zusammengesetzter Bezeichner für ein Objekt, das in der Regel eine Meldung in einem Nachrichtenspeicher. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a>Parameter

 _psession_
  
> [in] Zeiger auf die Sitzung von der Clientanwendung verwendet. 
    
 _cbStoreRecordKey_
  
> [in] Größe des Schlüssels Datensatz des Nachrichtenspeichers aufbewahren der Nachricht oder eines anderen Objekts in Bytes. Wenn 0 (null) der _PpEID_ -Parameter verweist auf eine Kopie des Eintrags-ID des Objekts in der _CbStoreRecordKey_ -Parameter übergeben wird. 
    
 _pStoreRecordKey_
  
> [in] Zeiger auf den Eintrag Schlüssel des Nachrichtenspeichers, die die Nachricht oder eines anderen Objekts enthält. 
    
 _cbMsgEID_
  
> [in] Größe des Eintrags-ID der Nachricht oder eines anderen Objekts in Bytes. 
    
 _pMsgEID_
  
> [in] Zeiger auf die Eintrags-ID des Objekts. 
    
 _pcbEID_
  
> [out] Zeiger auf die Größe des zurückgegebene Bezeichner in Bytes. 
    
 _ppEID_
  
> [out] Zeiger auf einen Zeiger auf den Bezeichner des zurückgegebenen Objekts. Wenn der Wert des Parameters _CbStoreRecordKey_ größer als NULL ist, zeigt der _PpEID_ -Parameter auf einen Zeiger auf das zusammengesetzter Eintrags-ID, die erstellt wird. Wenn _CbStoreRecordKey_ gleich NULL ist, zeigt _PpEID_ auf einen Zeiger auf eine Kopie des Eintrags-ID für das Objekt. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Bemerkungen

Wenn die Nachricht oder eines anderen Objekts für die die zusammengesetzter Eintrags-ID erstellt wird in einem Nachrichtenspeicher befindet, ist der Bezeichner aus Eintrags-ID für das Objekt und den Store-Eintrag Schlüssel erstellt. Ist das Objekt nicht in einem Speicher, d. h., wird Wenn die Byteanzahl für den Store-Eintrag Schlüssel übergebenen _CbStoreRecordKey_ 0 (null) ist, ist das Objekt Eintrags-ID einfach kopiert. 
  
Die Funktion **HrComposeEID** ermöglicht, dass Anwendungen-Objekte in mehreren Informationsspeichern mithilfe von zusammengesetzten-Eintragsbezeichner entwickelt. Eine Anwendung kann die [HrDecomposeEID](hrdecomposeeid.md) -Funktion, um die zusammengesetzter Eintrags-ID in seiner ursprünglichen Bestandteile aufgeteilt aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

