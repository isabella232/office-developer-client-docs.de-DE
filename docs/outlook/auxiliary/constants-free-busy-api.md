---
title: Konstanten (frei/gebucht-API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Dieses Thema enthält Konstante Definitionen, Klassenbezeichner und Schnittstellenbezeichner für die Frei/Gebucht-API.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431533"
---
# <a name="constants-freebusy-api"></a>Konstanten (frei/gebucht-API)

Dieses Thema enthält Konstante Definitionen, Klassenbezeichner und Schnittstellenbezeichner für die Frei/Gebucht-API.
  
## <a name="constants"></a>Konstanten

|**Konstante**|**Definition**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Gemäß der Definition in der Microsoft Windows Software Development Kit (SDK)-Headerdatei Winerror. h.*  <br/> |
|E_OUTOFMEMORY  <br/> | *Gemäß der Definition in der Windows SDK-Headerdatei Winerror. h.*  <br/> |
|S_FALSE  <br/> | *Gemäß der Definition in der Windows SDK-Headerdatei Winerror. h.*  <br/> |
|S_OK  <br/> | *Gemäß der Definition in der Windows SDK-Headerdatei Winerror. h.*  <br/> |
   
## <a name="interface-identifiers"></a>Schnittstellenbezeichner

Für die folgenden Schnittstellenbezeichner wird davon ausgegangen, dass das DEFINE_GUID-Makro, das in der Windows SDK-Headerdatei guiddef. h definiert ist, den symbolischen GUID-Namen mit seinem Wert verknüpft.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0x0 festlegen, 0x0 festlegen, 0xC0, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0x0 festlegen, 0x0 festlegen, 0xC0, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0x0 festlegen, 0x0 festlegen, 0xC0, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x0 festlegen, 0x46);
  

