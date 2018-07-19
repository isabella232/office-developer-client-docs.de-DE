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
ms.openlocfilehash: a89b1a93b2b03f97426a3988739e9b0d8411f113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792049"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="eb21c-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb21c-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="eb21c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb21c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb21c-105">Ermöglicht die Konvertierung zwischen MIME-Objekten und MAPI-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="eb21c-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="eb21c-106">Dies kann insbesondere für die Übermittlung von Nachrichten über das Internet sein.</span><span class="sxs-lookup"><span data-stu-id="eb21c-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eb21c-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="eb21c-107">Provided by:</span></span>  <br/> |<span data-ttu-id="eb21c-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="eb21c-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="eb21c-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="eb21c-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eb21c-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="eb21c-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="eb21c-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="eb21c-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb21c-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="eb21c-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="eb21c-113">Gibt ein optionales MAPI-Adressbuch, die MAPI zu MIME-Konverter verwendet, um mehrdeutige Adressen aufzulösen, beim Konvertieren einer MAPI-Nachricht in eine MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="eb21c-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="eb21c-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="eb21c-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="eb21c-115">Initialisiert die während der Konvertierung zu verwendende Codierung.</span><span class="sxs-lookup"><span data-stu-id="eb21c-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="eb21c-116">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="eb21c-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="eb21c-117">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="eb21c-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="eb21c-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="eb21c-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="eb21c-119">Konvertiert einen MIME-Datenstrom an einem MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="eb21c-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="eb21c-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="eb21c-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="eb21c-121">Konvertiert eine MAPI-Nachricht in einen MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="eb21c-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="eb21c-122">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="eb21c-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="eb21c-123">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="eb21c-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="eb21c-124">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="eb21c-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="eb21c-125">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="eb21c-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="eb21c-126">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="eb21c-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="eb21c-127">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="eb21c-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="eb21c-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="eb21c-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="eb21c-129">Legt den Textfluss Breite für einen MIME-Stream, den der Konverter in **MAPIToMIMEStm**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="eb21c-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="eb21c-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="eb21c-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="eb21c-131">Legt das Format an, dass der Konverter einen MIME-Stream in **MAPIToMIMEStm**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb21c-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="eb21c-132">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="eb21c-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="eb21c-133">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="eb21c-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="eb21c-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="eb21c-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="eb21c-135">Gibt an, dass ein optionales Zeichen festgelegt, dass die MAPI zu MIME-Konverter, beim Konvertieren einer MAPI-Nachricht in eine MIME-Stream verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb21c-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eb21c-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="eb21c-136">Remarks</span></span>

<span data-ttu-id="eb21c-137">Rufen Sie **SetEncoding** vor der Nutzung **MAPIToMIMEStm** Konvertierung ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb21c-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb21c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb21c-138">See also</span></span>



[<span data-ttu-id="eb21c-139">Informationen über die MAPI-MIME-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="eb21c-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="eb21c-140">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="eb21c-140">MAPI Constants</span></span>](mapi-constants.md)

