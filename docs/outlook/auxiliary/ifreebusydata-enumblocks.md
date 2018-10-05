---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Ruft eine Schnittstelle, die Datenblöcke Frei/Gebucht-Informationen für einen Benutzer in einen angegebenen Zeitraum auflistet.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394538"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Ruft eine Schnittstelle, die Datenblöcke Frei/Gebucht-Informationen für einen Benutzer in einen angegebenen Zeitraum auflistet.
  
## <a name="quick-info"></a>QuickInfo

Finden Sie unter [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parameter

_ppenumfb_
  
> [out] Eine Schnittstelle zum Aufzählen von Frei/Gebucht-Blöcke.
    
_ftmStart_
  
> [in] Die Startzeit für die Enumeration. Es wird in [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)ausgedrückt.
    
_ftmEnd_
  
> [in] Die Endzeit für die Enumeration. Es wird in **FILETIME**ausgedrückt. 
    
## <a name="return-values"></a>Rückgabewerte

S_OK zurück, wenn der Aufruf erfolgreich war; andernfalls einen Fehlercode.
  
## <a name="remarks"></a>Anmerkungen

Diese Methode wird verwendet, um den Zeitbereich des Kalenderelemente für das Abrufen von Details anzuzeigen. Die Werte der *FtmStart* und *FtmEnd* werden zwischengespeichert und in einem nachfolgenden Aufruf der [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)zurückgegeben.
  
Ein Anbieter Frei/Gebucht-Informationen kann auch anschließend die zurückgegebene [IEnumFBBlock](ienumfbblock.md) -Schnittstelle verwenden, um Zugriff auf die-Aufzählung. 
  
## <a name="see-also"></a>Siehe auch

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)

