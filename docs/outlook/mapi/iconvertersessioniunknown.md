---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432317"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="344d7-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="344d7-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="344d7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="344d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="344d7-105">Ermöglicht Konvertierungen zwischen MIME-Objekten und MAPI-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="344d7-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="344d7-106">Dies kann beim Transport von Nachrichten über das Internet hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="344d7-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="344d7-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="344d7-107">Provided by:</span></span>  <br/> |<span data-ttu-id="344d7-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="344d7-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="344d7-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="344d7-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="344d7-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="344d7-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="344d7-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="344d7-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="344d7-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="344d7-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="344d7-113">Gibt ein optionales MAPI-Adressbuch an, das der MAPI-zu-MIME-Konverter zum Auflösen mehrdeutiger Adressen beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream verwendet.</span><span class="sxs-lookup"><span data-stu-id="344d7-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="344d7-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="344d7-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="344d7-115">Initialisiert die während der Konvertierung zu verwendende Codierung.</span><span class="sxs-lookup"><span data-stu-id="344d7-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="344d7-116">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="344d7-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="344d7-117">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="344d7-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="344d7-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="344d7-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="344d7-119">Konvertiert einen MIME-Stream in eine MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="344d7-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="344d7-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="344d7-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="344d7-121">Konvertiert eine MAPI-Nachricht in einen MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="344d7-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="344d7-122">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="344d7-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="344d7-123">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="344d7-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="344d7-124">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="344d7-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="344d7-125">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="344d7-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="344d7-126">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="344d7-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="344d7-127">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="344d7-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="344d7-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="344d7-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="344d7-129">Legt die Textumbruchbreite für einen MIME-Stream fest, den der Konverter in **MAPIToMIMEStm zurückgibt.**</span><span class="sxs-lookup"><span data-stu-id="344d7-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="344d7-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="344d7-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="344d7-131">Legt das Format fest, das der Konverter einen MIME-Stream in **MAPIToMIMEStm zurückgibt.**</span><span class="sxs-lookup"><span data-stu-id="344d7-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="344d7-132">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="344d7-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="344d7-133">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="344d7-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="344d7-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="344d7-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="344d7-135">Gibt einen optionalen Zeichensatz an, den der MAPI-zu-MIME-Konverter beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream verwendet.</span><span class="sxs-lookup"><span data-stu-id="344d7-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="344d7-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="344d7-136">Remarks</span></span>

<span data-ttu-id="344d7-137">Rufen **Sie SetEncoding auf,** bevor Sie **MAPIToMIMEStm** zum Ausführen der Konvertierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="344d7-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="344d7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="344d7-138">See also</span></span>



[<span data-ttu-id="344d7-139">Informationen über die MAPI-MIME-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="344d7-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="344d7-140">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="344d7-140">MAPI Constants</span></span>](mapi-constants.md)

