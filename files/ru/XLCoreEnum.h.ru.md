Title: XLCoreEnum.h


# XENOLITH_CORE_XLCOREENUM_H_

## BRIEF

Перечислимые типы

## CONTENT

Перечислимые типы

# ::stappler::xenolith::core::FrameRenderPassState

## BRIEF

Состояние конечного автомата прохода рендеринга

## CONTENT

Состояние конечного автомата прохода рендеринга

Значения:
* Initial
* Ready
* Owned
* ResourcesAcquired
* Prepared
* Submission
* Submitted
* Complete
* Finalized


# ::stappler::xenolith::core::FrameAttachmentState

## BRIEF

Состояние конечного автомата вложения

## CONTENT

Состояние конечного автомата вложения

Значения:
* Initial
* Setup
* InputRequired
* Ready
* ResourcesPending
* ResourcesAcquired
* Detached
* Complete
* ResourcesReleased
* Finalized


# ::stappler::xenolith::core::AttachmentType

## BRIEF

Тип вложения

## CONTENT

Тип вложения

Значения:
* Image
* Buffer
* Generic


# ::stappler::xenolith::core::PipelineStage

## BRIEF

Стадия пайплайна

## CONTENT

Стадия пайплайна. Копирует VkPipelineStageFlagBits

Значения:
* None
* TopOfPipe
* DrawIndirect
* VertexInput
* VertexShader
* TesselationControl
* TesselationEvaluation
* GeometryShader
* FragmentShader
* EarlyFragmentTest
* LateFragmentTest
* ColorAttachmentOutput
* ComputeShader
* Transfer
* BottomOfPipe
* Host
* AllGraphics
* AllCommands
* TransformFeedback
* ConditionalRendering
* AccelerationStructureBuild
* RayTracingShader
* ShadingRateImage
* TaskShader
* MeshShader
* FragmentDensityProcess
* CommandPreprocess


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::PipelineStage const&,stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage const&
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* stappler::xenolith::core::PipelineStage

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::PipelineStage const&,stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage const&
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* stappler::xenolith::core::PipelineStage

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::PipelineStage const&,stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage const&
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* stappler::xenolith::core::PipelineStage

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::PipelineStage&,stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage&
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* stappler::xenolith::core::PipelineStage&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::PipelineStage&,stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage&
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* stappler::xenolith::core::PipelineStage&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::PipelineStage&,stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage&
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* stappler::xenolith::core::PipelineStage&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::PipelineStage const&,std::underlying_type<PipelineStage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage const&
* std::underlying_type<PipelineStage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<PipelineStage>::type const&,stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<PipelineStage>::type const&
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::PipelineStage const&,std::underlying_type<PipelineStage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage const&
* std::underlying_type<PipelineStage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<PipelineStage>::type const&,stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<PipelineStage>::type const&
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::PipelineStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::PipelineStage const&

Возвращает:
* stappler::xenolith::core::PipelineStage

# ::stappler::xenolith::core::AccessType

## BRIEF

Тип доступа к данным

## CONTENT

Тип доступа к данным. Копирует VkAccessFlag

Значения:
* None
* IndirectCommandRead
* IndexRead
* VertexAttributeRead
* UniformRead
* InputAttachmantRead
* ShaderRead
* ShaderWrite
* ColorAttachmentRead
* ColorAttachmentWrite
* DepthStencilAttachmentRead
* DepthStencilAttachmentWrite
* TransferRead
* TransferWrite
* HostRead
* HostWrite
* MemoryRead
* MemoryWrite
* TransformFeedbackWrite
* TransformFeedbackCounterRead
* TransformFeedbackCounterWrite
* ConditionalRenderingRead
* ColorAttachmentReadNonCoherent
* AccelerationStructureRead
* AccelerationStructureWrite
* ShadingRateImageRead
* FragmentDensityMapRead
* CommandPreprocessRead
* CommandPreprocessWrite


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::AccessType const&,stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType const&
* stappler::xenolith::core::AccessType const&

Возвращает:
* stappler::xenolith::core::AccessType

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::AccessType const&,stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType const&
* stappler::xenolith::core::AccessType const&

Возвращает:
* stappler::xenolith::core::AccessType

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::AccessType const&,stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType const&
* stappler::xenolith::core::AccessType const&

Возвращает:
* stappler::xenolith::core::AccessType

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::AccessType&,stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType&
* stappler::xenolith::core::AccessType const&

Возвращает:
* stappler::xenolith::core::AccessType&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::AccessType&,stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType&
* stappler::xenolith::core::AccessType const&

Возвращает:
* stappler::xenolith::core::AccessType&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::AccessType&,stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType&
* stappler::xenolith::core::AccessType const&

Возвращает:
* stappler::xenolith::core::AccessType&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::AccessType const&,std::underlying_type<AccessType>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType const&
* std::underlying_type<AccessType>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<AccessType>::type const&,stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<AccessType>::type const&
* stappler::xenolith::core::AccessType const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::AccessType const&,std::underlying_type<AccessType>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType const&
* std::underlying_type<AccessType>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<AccessType>::type const&,stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<AccessType>::type const&
* stappler::xenolith::core::AccessType const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::AccessType const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AccessType const&

Возвращает:
* stappler::xenolith::core::AccessType

# ::stappler::xenolith::core::AttachmentOps

## BRIEF

Операции, выполняемые над вложением во время прохода и очереди

## CONTENT

Операции, выполняемые над вложением во время прохода и очереди

Значения:
* Undefined
* ReadColor
* ReadStencil
* WritesColor
* WritesStencil


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::AttachmentOps const&,stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps const&
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* stappler::xenolith::core::AttachmentOps

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::AttachmentOps const&,stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps const&
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* stappler::xenolith::core::AttachmentOps

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::AttachmentOps const&,stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps const&
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* stappler::xenolith::core::AttachmentOps

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::AttachmentOps&,stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps&
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* stappler::xenolith::core::AttachmentOps&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::AttachmentOps&,stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps&
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* stappler::xenolith::core::AttachmentOps&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::AttachmentOps&,stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps&
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* stappler::xenolith::core::AttachmentOps&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::AttachmentOps const&,std::underlying_type<AttachmentOps>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps const&
* std::underlying_type<AttachmentOps>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<AttachmentOps>::type const&,stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<AttachmentOps>::type const&
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::AttachmentOps const&,std::underlying_type<AttachmentOps>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps const&
* std::underlying_type<AttachmentOps>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<AttachmentOps>::type const&,stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<AttachmentOps>::type const&
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::AttachmentOps const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentOps const&

Возвращает:
* stappler::xenolith::core::AttachmentOps

# ::stappler::xenolith::core::AttachmentLoadOp

## BRIEF

Операция начальной загрузки вложения

## CONTENT

Операция начальной загрузки вложения. Копирует VkAttachmentLoadOp

Значения:
* Load
* Clear
* DontCare


# ::stappler::xenolith::core::AttachmentStoreOp

## BRIEF

Операция сохранения вложения

## CONTENT

Операция сохранения вложения. Копирует VkAttachmentStoreOp

Значения:
* Store
* DontCare


# ::stappler::xenolith::core::AttachmentUsage

## BRIEF

Способ использования вложения

## CONTENT

Способ использования вложения

Значения:
* None
* Input
* Output
* InputOutput
* Resolve
* DepthStencil
* InputDepthStencil


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::AttachmentUsage const&,stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage const&
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* stappler::xenolith::core::AttachmentUsage

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::AttachmentUsage const&,stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage const&
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* stappler::xenolith::core::AttachmentUsage

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::AttachmentUsage const&,stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage const&
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* stappler::xenolith::core::AttachmentUsage

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::AttachmentUsage&,stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage&
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* stappler::xenolith::core::AttachmentUsage&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::AttachmentUsage&,stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage&
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* stappler::xenolith::core::AttachmentUsage&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::AttachmentUsage&,stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage&
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* stappler::xenolith::core::AttachmentUsage&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::AttachmentUsage const&,std::underlying_type<AttachmentUsage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage const&
* std::underlying_type<AttachmentUsage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<AttachmentUsage>::type const&,stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<AttachmentUsage>::type const&
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::AttachmentUsage const&,std::underlying_type<AttachmentUsage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage const&
* std::underlying_type<AttachmentUsage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<AttachmentUsage>::type const&,stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<AttachmentUsage>::type const&
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::AttachmentUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::AttachmentUsage const&

Возвращает:
* stappler::xenolith::core::AttachmentUsage

# ::stappler::xenolith::core::DescriptorType

## BRIEF

Тип дескриптора

## CONTENT

Тип дескриптора. Копирует VkDescriptorType

Значения:
* Sampler
* CombinedImageSampler
* SampledImage
* StorageImage
* UniformTexelBuffer
* StorageTexelBuffer
* UniformBuffer
* StorageBuffer
* UniformBufferDynamic
* StorageBufferDynamic
* InputAttachment
* Attachment
* Unknown


# ::stappler::xenolith::core::ProgramStage

## BRIEF

Стадия исполнения подпрограммы

## CONTENT

Стадия исполнения подпрограммы. Копирует VkShaderStageFlagBits

Значения:
* None
* Vertex
* TesselationControl
* TesselationEvaluation
* Geometry
* Fragment
* Compute
* RayGen
* AnyHit
* ClosestHit
* MissHit
* Intersection
* Callable
* Task
* Mesh


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::ProgramStage const&,stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage const&
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* stappler::xenolith::core::ProgramStage

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::ProgramStage const&,stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage const&
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* stappler::xenolith::core::ProgramStage

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::ProgramStage const&,stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage const&
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* stappler::xenolith::core::ProgramStage

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::ProgramStage&,stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage&
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* stappler::xenolith::core::ProgramStage&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::ProgramStage&,stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage&
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* stappler::xenolith::core::ProgramStage&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::ProgramStage&,stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage&
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* stappler::xenolith::core::ProgramStage&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::ProgramStage const&,std::underlying_type<ProgramStage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage const&
* std::underlying_type<ProgramStage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<ProgramStage>::type const&,stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ProgramStage>::type const&
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::ProgramStage const&,std::underlying_type<ProgramStage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage const&
* std::underlying_type<ProgramStage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<ProgramStage>::type const&,stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ProgramStage>::type const&
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::ProgramStage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ProgramStage const&

Возвращает:
* stappler::xenolith::core::ProgramStage

# ::stappler::xenolith::core::AttachmentLayout

## BRIEF

Способ укладки изображения в памяти устройства

## CONTENT

Способ укладки изображения в памяти устройства. Копирует VkImageLayout

Значения:
* Undefined
* General
* ColorAttachmentOptimal
* DepthStencilAttachmentOptimal
* DepthStencilReadOnlyOptimal
* ShaderReadOnlyOptimal
* TransferSrcOptimal
* TransferDstOptimal
* Preinitialized
* DepthReadOnlyStencilAttachmentOptimal
* DepthAttachmentStencilReadOnlyOptimal
* DepthAttachmentOptimal
* DepthReadOnlyOptimal
* StencilAttachmentOptimal
* StencilReadOnlyOptimal
* PresentSrc
* Ignored


# ::stappler::xenolith::core::PassType

## BRIEF

Тип прохода исполнения

## CONTENT

Тип прохода исполнения

Значения:
* Graphics - графический
* Compute - вычислительный
* Transfer - трансферный
* Generic - пользовательский


# ::stappler::xenolith::core::PredefinedConstant

## BRIEF

Тип предопределённой внутри устройства константы

## CONTENT

Тип предопределённой внутри устройства константы

Значения:
* SamplersArraySize - число семплеров
* SamplersDescriptorIdx - индекс дескриптора семплеров
* TexturesArraySize - размер массива укладки текстур
* TexturesDescriptorIdx - индекс привязки массива текстур
* BuffersArraySize - размер массива дополнительных буферов
* BuffersDescriptorIdx - индекс привязки дополнительных бферов
* CurrentSamplerIdx - текущий используемый семплер по умолчанию


# ::stappler::xenolith::core::SpecializationConstant

## BRIEF

Структура константы специализации

## CONTENT

Структура константы специализации


# ::stappler::xenolith::core::SpecializationConstant::Type

## BRIEF

Тип константы

## CONTENT

Тип константы

Значения:
* Int
* Float
* Predefined


# ::stappler::xenolith::core::SpecializationConstant::type

## BRIEF

Тип константы

## CONTENT

Тип константы

Тип: stappler::xenolith::core::SpecializationConstant::Type


# ::stappler::xenolith::core::SpecializationConstant::

## BRIEF

Объединение данных

## CONTENT

Объединение данных


# ::stappler::xenolith::core::SpecializationConstant::intValue

## BRIEF

Целое число

## CONTENT

Целое число

Тип: int


# ::stappler::xenolith::core::SpecializationConstant::floatValue

## BRIEF

Число с плавающей точкой

## CONTENT

Число с плавающей точкой

Тип: float


# ::stappler::xenolith::core::SpecializationConstant::predefinedValue

## BRIEF

Предопределённое значение

## CONTENT

Предопределённое значение

Тип: stappler::xenolith::core::PredefinedConstant


# ::stappler::xenolith::core::SpecializationConstant::SpecializationConstant(int)

## BRIEF

Конструктор

## CONTENT

Конструктор

Параметры:
* int


# ::stappler::xenolith::core::SpecializationConstant::SpecializationConstant(uint32_t)

## BRIEF

Конструктор

## CONTENT

Конструктор

Параметры:
* uint32_t


# ::stappler::xenolith::core::SpecializationConstant::SpecializationConstant(float)

## BRIEF

Конструктор

## CONTENT

Конструктор

Параметры:
* float


# ::stappler::xenolith::core::SpecializationConstant::SpecializationConstant(stappler::xenolith::core::PredefinedConstant)

## BRIEF

Конструктор

## CONTENT

Конструктор

Параметры:
* stappler::xenolith::core::PredefinedConstant


# ::stappler::xenolith::core::DynamicState

## BRIEF

Флаги динамических режимов

## CONTENT

Флаги динамических режимов

Значения:
* None
* Viewport
* Scissor
* Default


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::DynamicState const&,stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState const&
* stappler::xenolith::core::DynamicState const&

Возвращает:
* stappler::xenolith::core::DynamicState

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::DynamicState const&,stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState const&
* stappler::xenolith::core::DynamicState const&

Возвращает:
* stappler::xenolith::core::DynamicState

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::DynamicState const&,stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState const&
* stappler::xenolith::core::DynamicState const&

Возвращает:
* stappler::xenolith::core::DynamicState

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::DynamicState&,stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState&
* stappler::xenolith::core::DynamicState const&

Возвращает:
* stappler::xenolith::core::DynamicState&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::DynamicState&,stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState&
* stappler::xenolith::core::DynamicState const&

Возвращает:
* stappler::xenolith::core::DynamicState&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::DynamicState&,stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState&
* stappler::xenolith::core::DynamicState const&

Возвращает:
* stappler::xenolith::core::DynamicState&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::DynamicState const&,std::underlying_type<DynamicState>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState const&
* std::underlying_type<DynamicState>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<DynamicState>::type const&,stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<DynamicState>::type const&
* stappler::xenolith::core::DynamicState const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::DynamicState const&,std::underlying_type<DynamicState>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState const&
* std::underlying_type<DynamicState>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<DynamicState>::type const&,stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<DynamicState>::type const&
* stappler::xenolith::core::DynamicState const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::DynamicState const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::DynamicState const&

Возвращает:
* stappler::xenolith::core::DynamicState

# ::stappler::xenolith::core::BufferFlags

## BRIEF

Флаги создания буфера

## CONTENT

Флаги создания буфера. Копирует VkBufferCreateFlagBits

Значения:
* None
* SparceBinding
* SparceResidency
* SparceAliased
* Protected


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::BufferFlags const&,stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags const&
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* stappler::xenolith::core::BufferFlags

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::BufferFlags const&,stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags const&
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* stappler::xenolith::core::BufferFlags

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::BufferFlags const&,stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags const&
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* stappler::xenolith::core::BufferFlags

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::BufferFlags&,stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags&
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* stappler::xenolith::core::BufferFlags&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::BufferFlags&,stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags&
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* stappler::xenolith::core::BufferFlags&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::BufferFlags&,stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags&
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* stappler::xenolith::core::BufferFlags&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::BufferFlags const&,std::underlying_type<BufferFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags const&
* std::underlying_type<BufferFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<BufferFlags>::type const&,stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<BufferFlags>::type const&
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::BufferFlags const&,std::underlying_type<BufferFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags const&
* std::underlying_type<BufferFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<BufferFlags>::type const&,stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<BufferFlags>::type const&
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::BufferFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferFlags const&

Возвращает:
* stappler::xenolith::core::BufferFlags

# ::stappler::xenolith::core::BufferUsage

## BRIEF

Флаги использования буфера

## CONTENT

Флаги использования буфера. Копирует VkBufferUsageFlagBits

Значения:
* None
* TransferSrc
* TransferDst
* UniformTexelBuffer
* StorageTexelBuffer
* UniformBuffer
* StorageBuffer
* IndexBuffer
* VertexBuffer
* IndirectBuffer
* ShaderDeviceAddress
* TransformFeedback
* TransformFeedbackCounter
* ConditionalRendering
* AccelerationStructureBuildInputReadOnly
* AccelerationStructureStorage
* ShaderBindingTable


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::BufferUsage const&,stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage const&
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* stappler::xenolith::core::BufferUsage

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::BufferUsage const&,stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage const&
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* stappler::xenolith::core::BufferUsage

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::BufferUsage const&,stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage const&
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* stappler::xenolith::core::BufferUsage

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::BufferUsage&,stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage&
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* stappler::xenolith::core::BufferUsage&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::BufferUsage&,stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage&
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* stappler::xenolith::core::BufferUsage&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::BufferUsage&,stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage&
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* stappler::xenolith::core::BufferUsage&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::BufferUsage const&,std::underlying_type<BufferUsage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage const&
* std::underlying_type<BufferUsage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<BufferUsage>::type const&,stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<BufferUsage>::type const&
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::BufferUsage const&,std::underlying_type<BufferUsage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage const&
* std::underlying_type<BufferUsage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<BufferUsage>::type const&,stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<BufferUsage>::type const&
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::BufferUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::BufferUsage const&

Возвращает:
* stappler::xenolith::core::BufferUsage

# ::stappler::xenolith::core::ImageFlags

## BRIEF

Флаги создания изображения

## CONTENT

Флаги создания изображения. Копирует VkImageCreateFlagBits.

Значения:
* None
* SparceBinding
* SparceResidency
* SparceAliased
* MutableFormat
* CubeCompatible
* Alias
* SplitInstanceBindRegions
* Array2dCompatible
* BlockTexelViewCompatible
* ExtendedUsage
* Protected
* Disjoint


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::ImageFlags const&,stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags const&
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* stappler::xenolith::core::ImageFlags

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::ImageFlags const&,stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags const&
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* stappler::xenolith::core::ImageFlags

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::ImageFlags const&,stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags const&
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* stappler::xenolith::core::ImageFlags

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::ImageFlags&,stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags&
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* stappler::xenolith::core::ImageFlags&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::ImageFlags&,stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags&
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* stappler::xenolith::core::ImageFlags&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::ImageFlags&,stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags&
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* stappler::xenolith::core::ImageFlags&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::ImageFlags const&,std::underlying_type<ImageFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags const&
* std::underlying_type<ImageFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<ImageFlags>::type const&,stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ImageFlags>::type const&
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::ImageFlags const&,std::underlying_type<ImageFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags const&
* std::underlying_type<ImageFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<ImageFlags>::type const&,stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ImageFlags>::type const&
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::ImageFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageFlags const&

Возвращает:
* stappler::xenolith::core::ImageFlags

# ::stappler::xenolith::core::SampleCount

## BRIEF

Число точек в пикселе изображения

## CONTENT

Число точек в пикселе изображения (для MSAA и подобного). Копирует VkSampleCountFlagBits.

Значения:
* None
* X1
* X2
* X4
* X8
* X16
* X32
* X64


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::SampleCount const&,stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount const&
* stappler::xenolith::core::SampleCount const&

Возвращает:
* stappler::xenolith::core::SampleCount

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::SampleCount const&,stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount const&
* stappler::xenolith::core::SampleCount const&

Возвращает:
* stappler::xenolith::core::SampleCount

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::SampleCount const&,stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount const&
* stappler::xenolith::core::SampleCount const&

Возвращает:
* stappler::xenolith::core::SampleCount

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::SampleCount&,stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount&
* stappler::xenolith::core::SampleCount const&

Возвращает:
* stappler::xenolith::core::SampleCount&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::SampleCount&,stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount&
* stappler::xenolith::core::SampleCount const&

Возвращает:
* stappler::xenolith::core::SampleCount&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::SampleCount&,stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount&
* stappler::xenolith::core::SampleCount const&

Возвращает:
* stappler::xenolith::core::SampleCount&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::SampleCount const&,std::underlying_type<SampleCount>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount const&
* std::underlying_type<SampleCount>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<SampleCount>::type const&,stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<SampleCount>::type const&
* stappler::xenolith::core::SampleCount const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::SampleCount const&,std::underlying_type<SampleCount>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount const&
* std::underlying_type<SampleCount>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<SampleCount>::type const&,stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<SampleCount>::type const&
* stappler::xenolith::core::SampleCount const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::SampleCount const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SampleCount const&

Возвращает:
* stappler::xenolith::core::SampleCount

# ::stappler::xenolith::core::ImageType

## BRIEF

Тип размерности изображения

## CONTENT

Тип размерности изображения. Копирует VkImageType.

Значения:
* Image1D
* Image2D
* Image3D


# ::stappler::xenolith::core::ImageViewType

## BRIEF

Тип размерности отображения изображения

## CONTENT

Тип размерности отображения изображения. Копирует VkImageViewType.

Значения:
* ImageView1D
* ImageView2D
* ImageView3D
* ImageViewCube
* ImageView1DArray
* ImageView2DArray
* ImageViewCubeArray


# ::stappler::xenolith::core::ImageFormat

## BRIEF

Формат изображения

## CONTENT

Формат изображения. Копирует VkFormat.

Значения:
* Undefined
* R4G4_UNORM_PACK8
* R4G4B4A4_UNORM_PACK16
* B4G4R4A4_UNORM_PACK16
* R5G6B5_UNORM_PACK16
* B5G6R5_UNORM_PACK16
* R5G5B5A1_UNORM_PACK16
* B5G5R5A1_UNORM_PACK16
* A1R5G5B5_UNORM_PACK16
* R8_UNORM
* R8_SNORM
* R8_USCALED
* R8_SSCALED
* R8_UINT
* R8_SINT
* R8_SRGB
* R8G8_UNORM
* R8G8_SNORM
* R8G8_USCALED
* R8G8_SSCALED
* R8G8_UINT
* R8G8_SINT
* R8G8_SRGB
* R8G8B8_UNORM
* R8G8B8_SNORM
* R8G8B8_USCALED
* R8G8B8_SSCALED
* R8G8B8_UINT
* R8G8B8_SINT
* R8G8B8_SRGB
* B8G8R8_UNORM
* B8G8R8_SNORM
* B8G8R8_USCALED
* B8G8R8_SSCALED
* B8G8R8_UINT
* B8G8R8_SINT
* B8G8R8_SRGB
* R8G8B8A8_UNORM
* R8G8B8A8_SNORM
* R8G8B8A8_USCALED
* R8G8B8A8_SSCALED
* R8G8B8A8_UINT
* R8G8B8A8_SINT
* R8G8B8A8_SRGB
* B8G8R8A8_UNORM
* B8G8R8A8_SNORM
* B8G8R8A8_USCALED
* B8G8R8A8_SSCALED
* B8G8R8A8_UINT
* B8G8R8A8_SINT
* B8G8R8A8_SRGB
* A8B8G8R8_UNORM_PACK32
* A8B8G8R8_SNORM_PACK32
* A8B8G8R8_USCALED_PACK32
* A8B8G8R8_SSCALED_PACK32
* A8B8G8R8_UINT_PACK32
* A8B8G8R8_SINT_PACK32
* A8B8G8R8_SRGB_PACK32
* A2R10G10B10_UNORM_PACK32
* A2R10G10B10_SNORM_PACK32
* A2R10G10B10_USCALED_PACK32
* A2R10G10B10_SSCALED_PACK32
* A2R10G10B10_UINT_PACK32
* A2R10G10B10_SINT_PACK32
* A2B10G10R10_UNORM_PACK32
* A2B10G10R10_SNORM_PACK32
* A2B10G10R10_USCALED_PACK32
* A2B10G10R10_SSCALED_PACK32
* A2B10G10R10_UINT_PACK32
* A2B10G10R10_SINT_PACK32
* R16_UNORM
* R16_SNORM
* R16_USCALED
* R16_SSCALED
* R16_UINT
* R16_SINT
* R16_SFLOAT
* R16G16_UNORM
* R16G16_SNORM
* R16G16_USCALED
* R16G16_SSCALED
* R16G16_UINT
* R16G16_SINT
* R16G16_SFLOAT
* R16G16B16_UNORM
* R16G16B16_SNORM
* R16G16B16_USCALED
* R16G16B16_SSCALED
* R16G16B16_UINT
* R16G16B16_SINT
* R16G16B16_SFLOAT
* R16G16B16A16_UNORM
* R16G16B16A16_SNORM
* R16G16B16A16_USCALED
* R16G16B16A16_SSCALED
* R16G16B16A16_UINT
* R16G16B16A16_SINT
* R16G16B16A16_SFLOAT
* R32_UINT
* R32_SINT
* R32_SFLOAT
* R32G32_UINT
* R32G32_SINT
* R32G32_SFLOAT
* R32G32B32_UINT
* R32G32B32_SINT
* R32G32B32_SFLOAT
* R32G32B32A32_UINT
* R32G32B32A32_SINT
* R32G32B32A32_SFLOAT
* R64_UINT
* R64_SINT
* R64_SFLOAT
* R64G64_UINT
* R64G64_SINT
* R64G64_SFLOAT
* R64G64B64_UINT
* R64G64B64_SINT
* R64G64B64_SFLOAT
* R64G64B64A64_UINT
* R64G64B64A64_SINT
* R64G64B64A64_SFLOAT
* B10G11R11_UFLOAT_PACK32
* E5B9G9R9_UFLOAT_PACK32
* D16_UNORM
* X8_D24_UNORM_PACK32
* D32_SFLOAT
* S8_UINT
* D16_UNORM_S8_UINT
* D24_UNORM_S8_UINT
* D32_SFLOAT_S8_UINT
* BC1_RGB_UNORM_BLOCK
* BC1_RGB_SRGB_BLOCK
* BC1_RGBA_UNORM_BLOCK
* BC1_RGBA_SRGB_BLOCK
* BC2_UNORM_BLOCK
* BC2_SRGB_BLOCK
* BC3_UNORM_BLOCK
* BC3_SRGB_BLOCK
* BC4_UNORM_BLOCK
* BC4_SNORM_BLOCK
* BC5_UNORM_BLOCK
* BC5_SNORM_BLOCK
* BC6H_UFLOAT_BLOCK
* BC6H_SFLOAT_BLOCK
* BC7_UNORM_BLOCK
* BC7_SRGB_BLOCK
* ETC2_R8G8B8_UNORM_BLOCK
* ETC2_R8G8B8_SRGB_BLOCK
* ETC2_R8G8B8A1_UNORM_BLOCK
* ETC2_R8G8B8A1_SRGB_BLOCK
* ETC2_R8G8B8A8_UNORM_BLOCK
* ETC2_R8G8B8A8_SRGB_BLOCK
* EAC_R11_UNORM_BLOCK
* EAC_R11_SNORM_BLOCK
* EAC_R11G11_UNORM_BLOCK
* EAC_R11G11_SNORM_BLOCK
* ASTC_4x4_UNORM_BLOCK
* ASTC_4x4_SRGB_BLOCK
* ASTC_5x4_UNORM_BLOCK
* ASTC_5x4_SRGB_BLOCK
* ASTC_5x5_UNORM_BLOCK
* ASTC_5x5_SRGB_BLOCK
* ASTC_6x5_UNORM_BLOCK
* ASTC_6x5_SRGB_BLOCK
* ASTC_6x6_UNORM_BLOCK
* ASTC_6x6_SRGB_BLOCK
* ASTC_8x5_UNORM_BLOCK
* ASTC_8x5_SRGB_BLOCK
* ASTC_8x6_UNORM_BLOCK
* ASTC_8x6_SRGB_BLOCK
* ASTC_8x8_UNORM_BLOCK
* ASTC_8x8_SRGB_BLOCK
* ASTC_10x5_UNORM_BLOCK
* ASTC_10x5_SRGB_BLOCK
* ASTC_10x6_UNORM_BLOCK
* ASTC_10x6_SRGB_BLOCK
* ASTC_10x8_UNORM_BLOCK
* ASTC_10x8_SRGB_BLOCK
* ASTC_10x10_UNORM_BLOCK
* ASTC_10x10_SRGB_BLOCK
* ASTC_12x10_UNORM_BLOCK
* ASTC_12x10_SRGB_BLOCK
* ASTC_12x12_UNORM_BLOCK
* ASTC_12x12_SRGB_BLOCK
* G8B8G8R8_422_UNORM
* B8G8R8G8_422_UNORM
* G8_B8_R8_3PLANE_420_UNORM
* G8_B8R8_2PLANE_420_UNORM
* G8_B8_R8_3PLANE_422_UNORM
* G8_B8R8_2PLANE_422_UNORM
* G8_B8_R8_3PLANE_444_UNORM
* R10X6_UNORM_PACK16
* R10X6G10X6_UNORM_2PACK16
* R10X6G10X6B10X6A10X6_UNORM_4PACK16
* G10X6B10X6G10X6R10X6_422_UNORM_4PACK16
* B10X6G10X6R10X6G10X6_422_UNORM_4PACK16
* G10X6_B10X6_R10X6_3PLANE_420_UNORM_3PACK16
* G10X6_B10X6R10X6_2PLANE_420_UNORM_3PACK16
* G10X6_B10X6_R10X6_3PLANE_422_UNORM_3PACK16
* G10X6_B10X6R10X6_2PLANE_422_UNORM_3PACK16
* G10X6_B10X6_R10X6_3PLANE_444_UNORM_3PACK16
* R12X4_UNORM_PACK16
* R12X4G12X4_UNORM_2PACK16
* R12X4G12X4B12X4A12X4_UNORM_4PACK16
* G12X4B12X4G12X4R12X4_422_UNORM_4PACK16
* B12X4G12X4R12X4G12X4_422_UNORM_4PACK16
* G12X4_B12X4_R12X4_3PLANE_420_UNORM_3PACK16
* G12X4_B12X4R12X4_2PLANE_420_UNORM_3PACK16
* G12X4_B12X4_R12X4_3PLANE_422_UNORM_3PACK16
* G12X4_B12X4R12X4_2PLANE_422_UNORM_3PACK16
* G12X4_B12X4_R12X4_3PLANE_444_UNORM_3PACK16
* G16B16G16R16_422_UNORM
* B16G16R16G16_422_UNORM
* G16_B16_R16_3PLANE_420_UNORM
* G16_B16R16_2PLANE_420_UNORM
* G16_B16_R16_3PLANE_422_UNORM
* G16_B16R16_2PLANE_422_UNORM
* G16_B16_R16_3PLANE_444_UNORM
* PVRTC1_2BPP_UNORM_BLOCK_IMG
* PVRTC1_4BPP_UNORM_BLOCK_IMG
* PVRTC2_2BPP_UNORM_BLOCK_IMG
* PVRTC2_4BPP_UNORM_BLOCK_IMG
* PVRTC1_2BPP_SRGB_BLOCK_IMG
* PVRTC1_4BPP_SRGB_BLOCK_IMG
* PVRTC2_2BPP_SRGB_BLOCK_IMG
* PVRTC2_4BPP_SRGB_BLOCK_IMG
* ASTC_4x4_SFLOAT_BLOCK_EXT
* ASTC_5x4_SFLOAT_BLOCK_EXT
* ASTC_5x5_SFLOAT_BLOCK_EXT
* ASTC_6x5_SFLOAT_BLOCK_EXT
* ASTC_6x6_SFLOAT_BLOCK_EXT
* ASTC_8x5_SFLOAT_BLOCK_EXT
* ASTC_8x6_SFLOAT_BLOCK_EXT
* ASTC_8x8_SFLOAT_BLOCK_EXT
* ASTC_10x5_SFLOAT_BLOCK_EXT
* ASTC_10x6_SFLOAT_BLOCK_EXT
* ASTC_10x8_SFLOAT_BLOCK_EXT
* ASTC_10x10_SFLOAT_BLOCK_EXT
* ASTC_12x10_SFLOAT_BLOCK_EXT
* ASTC_12x12_SFLOAT_BLOCK_EXT
* G8_B8R8_2PLANE_444_UNORM_EXT
* G10X6_B10X6R10X6_2PLANE_444_UNORM_3PACK16_EXT
* G12X4_B12X4R12X4_2PLANE_444_UNORM_3PACK16_EXT
* G16_B16R16_2PLANE_444_UNORM_EXT
* A4R4G4B4_UNORM_PACK16_EXT
* A4B4G4R4_UNORM_PACK16_EXT


# ::stappler::xenolith::core::ColorSpace

## BRIEF

Тип цветового пространства

## CONTENT

Тип цветового пространства. Копирует VkColorSpaceKHR.

Значения:
* SRGB_NONLINEAR_KHR
* DISPLAY_P3_NONLINEAR_EXT
* EXTENDED_SRGB_LINEAR_EXT
* DISPLAY_P3_LINEAR_EXT
* DCI_P3_NONLINEAR_EXT
* BT709_LINEAR_EXT
* BT709_NONLINEAR_EXT
* BT2020_LINEAR_EXT
* HDR10_ST2084_EXT
* DOLBYVISION_EXT
* HDR10_HLG_EXT
* ADOBERGB_LINEAR_EXT
* ADOBERGB_NONLINEAR_EXT
* PASS_THROUGH_EXT
* EXTENDED_SRGB_NONLINEAR_EXT
* DISPLAY_NATIVE_AMD


# ::stappler::xenolith::core::CompositeAlphaFlags

## BRIEF

Способ совмещения альфаканала с системным

## CONTENT

Способ совмещения альфаканала с системным. Копирует VkCompositeAlphaFlagBitsKHR.

Значения:
* None
* Opaque
* Premultiplied
* Postmultiplied
* Inherit


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::CompositeAlphaFlags const&,stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags const&
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* stappler::xenolith::core::CompositeAlphaFlags

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::CompositeAlphaFlags const&,stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags const&
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* stappler::xenolith::core::CompositeAlphaFlags

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::CompositeAlphaFlags const&,stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags const&
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* stappler::xenolith::core::CompositeAlphaFlags

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::CompositeAlphaFlags&,stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags&
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* stappler::xenolith::core::CompositeAlphaFlags&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::CompositeAlphaFlags&,stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags&
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* stappler::xenolith::core::CompositeAlphaFlags&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::CompositeAlphaFlags&,stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags&
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* stappler::xenolith::core::CompositeAlphaFlags&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::CompositeAlphaFlags const&,std::underlying_type<CompositeAlphaFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags const&
* std::underlying_type<CompositeAlphaFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<CompositeAlphaFlags>::type const&,stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<CompositeAlphaFlags>::type const&
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::CompositeAlphaFlags const&,std::underlying_type<CompositeAlphaFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags const&
* std::underlying_type<CompositeAlphaFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<CompositeAlphaFlags>::type const&,stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<CompositeAlphaFlags>::type const&
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::CompositeAlphaFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::CompositeAlphaFlags const&

Возвращает:
* stappler::xenolith::core::CompositeAlphaFlags

# ::stappler::xenolith::core::ImageTiling

## BRIEF

Режим структурирования изображения

## CONTENT

Режим структурирования изображения. Копирует VkImageTiling.

Значения:
* Optimal
* Linear


# ::stappler::xenolith::core::ImageUsage

## BRIEF

Флаги использования изображения

## CONTENT

Флаги использования изображения. Копирует VkImageUsageFlagBits.

Значения:
* None
* TransferSrc
* TransferDst
* Sampled
* Storage
* ColorAttachment
* DepthStencilAttachment
* TransientAttachment
* InputAttachment


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::ImageUsage const&,stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage const&
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* stappler::xenolith::core::ImageUsage

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::ImageUsage const&,stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage const&
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* stappler::xenolith::core::ImageUsage

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::ImageUsage const&,stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage const&
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* stappler::xenolith::core::ImageUsage

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::ImageUsage&,stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage&
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* stappler::xenolith::core::ImageUsage&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::ImageUsage&,stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage&
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* stappler::xenolith::core::ImageUsage&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::ImageUsage&,stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage&
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* stappler::xenolith::core::ImageUsage&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::ImageUsage const&,std::underlying_type<ImageUsage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage const&
* std::underlying_type<ImageUsage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<ImageUsage>::type const&,stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ImageUsage>::type const&
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::ImageUsage const&,std::underlying_type<ImageUsage>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage const&
* std::underlying_type<ImageUsage>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<ImageUsage>::type const&,stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ImageUsage>::type const&
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::ImageUsage const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageUsage const&

Возвращает:
* stappler::xenolith::core::ImageUsage

# ::stappler::xenolith::core::PresentMode

## BRIEF

Способ презентации изображения

## CONTENT

Способ презентации изображения

Значения:
* Unsupported
* Immediate
* FifoRelaxed
* Fifo
* Mailbox


# ::stappler::xenolith::core::AttachmentStorageType

## BRIEF

Режим хранения данных вложения

## CONTENT

Режим хранения данных вложения

Значения:
* Transient - переходный, не хранится вне кадра
* FrameStateless - не имеет состояния вне кадра. Имеет состояние на уровне кадра.
* ObjectStateless - не имеет состояния на уровне объекта в целом
* Stateful - имеет постоянно хранимое состояние


# ::stappler::xenolith::core::ImageHints

## BRIEF

Вспомогательные флаги для изображения

## CONTENT

Вспомогательные флаги для изображения

Значения:
* None
* Opaque - считать изображение непрозрачным
* FixedSize - изображение фиксированного размера (не изменять под кадр)
* DoNotCache - не кешировать изображение
* ReadOnly - изображение доступно только для чтения
* Static - изображение хранится статически


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::ImageHints const&,stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints const&
* stappler::xenolith::core::ImageHints const&

Возвращает:
* stappler::xenolith::core::ImageHints

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::ImageHints const&,stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints const&
* stappler::xenolith::core::ImageHints const&

Возвращает:
* stappler::xenolith::core::ImageHints

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::ImageHints const&,stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints const&
* stappler::xenolith::core::ImageHints const&

Возвращает:
* stappler::xenolith::core::ImageHints

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::ImageHints&,stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints&
* stappler::xenolith::core::ImageHints const&

Возвращает:
* stappler::xenolith::core::ImageHints&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::ImageHints&,stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints&
* stappler::xenolith::core::ImageHints const&

Возвращает:
* stappler::xenolith::core::ImageHints&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::ImageHints&,stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints&
* stappler::xenolith::core::ImageHints const&

Возвращает:
* stappler::xenolith::core::ImageHints&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::ImageHints const&,std::underlying_type<ImageHints>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints const&
* std::underlying_type<ImageHints>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<ImageHints>::type const&,stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ImageHints>::type const&
* stappler::xenolith::core::ImageHints const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::ImageHints const&,std::underlying_type<ImageHints>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints const&
* std::underlying_type<ImageHints>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<ImageHints>::type const&,stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ImageHints>::type const&
* stappler::xenolith::core::ImageHints const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::ImageHints const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ImageHints const&

Возвращает:
* stappler::xenolith::core::ImageHints

# ::stappler::xenolith::core::ComponentMapping

## BRIEF

Указатель на цветовой компонент

## CONTENT

Указатель на цветовой компонент. Копирует VkComponentSwizzle.

Значения:
* Identity - не менять
* Zero - всегда 0
* One - всегда полный цвет
* R - канал красного
* G - канал зелёного
* B - канал синего
* A - альфаканал


# ::stappler::xenolith::core::Filter

## BRIEF

Тип фильтрации для семплера

## CONTENT

Тип фильтрации для семплера. Копирует VkFilter.

Значения:
* Nearest
* Linear
* Cubic


# ::stappler::xenolith::core::SamplerMipmapMode

## BRIEF

Дальностный фильтр семплера

## CONTENT

Дальностный фильтр семплера. Копирует VkSamplerMipmapMode.

Значения:
* Nearest
* Linear


# ::stappler::xenolith::core::SamplerAddressMode

## BRIEF

Тип адресации семплера

## CONTENT

Тип адресации семплера. Копирует VkSamplerAddressMode.

Значения:
* Repeat
* MirroredRepeat
* ClampToEdge
* ClampToBorder


# ::stappler::xenolith::core::CompareOp

## BRIEF

Операция сравнения

## CONTENT

Операция сравнения. Копирует VkCompareOp.

Значения:
* Never
* Less
* Equal
* LessOrEqual
* Greater
* NotEqual
* GreaterOrEqual
* Always


# ::stappler::xenolith::core::BlendFactor

## BRIEF

Способ смещивания цвета

## CONTENT

Способ смещивания цвета. Копирует VkBlendFactor.

Значения:
* Zero
* One
* SrcColor
* OneMinusSrcColor
* DstColor
* OneMinusDstColor
* SrcAlpha
* OneMinusSrcAlpha
* DstAlpha
* OneMinusDstAlpha


# ::stappler::xenolith::core::BlendOp

## BRIEF

Операция смешивания

## CONTENT

Операция смешивания. Копирует VkBlendOp.

Значения:
* Add
* Subtract
* ReverseSubtract
* Min
* Max


# ::stappler::xenolith::core::ColorComponentFlags

## BRIEF

Флаги цветового компонента

## CONTENT

Флаги цветового компонента

Значения:
* R
* G
* B
* A
* All


# ::stappler::xenolith::core::StencilOp

## BRIEF

Операция для трафарета

## CONTENT

Операция для трафарета

Значения:
* Keep
* Zero
* Replace
* IncrementAndClamp
* DecrementAndClamp
* Invert
* InvertAndWrap
* DecrementAndWrap


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::ColorComponentFlags const&,stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags const&
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* stappler::xenolith::core::ColorComponentFlags

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::ColorComponentFlags const&,stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags const&
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* stappler::xenolith::core::ColorComponentFlags

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::ColorComponentFlags const&,stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags const&
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* stappler::xenolith::core::ColorComponentFlags

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::ColorComponentFlags&,stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags&
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* stappler::xenolith::core::ColorComponentFlags&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::ColorComponentFlags&,stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags&
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* stappler::xenolith::core::ColorComponentFlags&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::ColorComponentFlags&,stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags&
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* stappler::xenolith::core::ColorComponentFlags&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::ColorComponentFlags const&,std::underlying_type<ColorComponentFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags const&
* std::underlying_type<ColorComponentFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<ColorComponentFlags>::type const&,stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ColorComponentFlags>::type const&
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::ColorComponentFlags const&,std::underlying_type<ColorComponentFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags const&
* std::underlying_type<ColorComponentFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<ColorComponentFlags>::type const&,stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<ColorComponentFlags>::type const&
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::ColorComponentFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::ColorComponentFlags const&

Возвращает:
* stappler::xenolith::core::ColorComponentFlags

# ::stappler::xenolith::core::SurfaceTransformFlags

## BRIEF

Способ трансфроманции поверхности для отрисовки

## CONTENT

Способ трансфроманции поверхности для отрисовки

Значения:
* None
* Identity
* Rotate90
* Rotate180
* Rotate270
* Mirror
* MirrorRotate90
* MirrorRotate180
* MirrorRotate270
* Inherit
* PreRotated
* TransformMask


# ::stappler::xenolith::core::operator|(stappler::xenolith::core::SurfaceTransformFlags const&,stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags const&
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* stappler::xenolith::core::SurfaceTransformFlags

# ::stappler::xenolith::core::operator&(stappler::xenolith::core::SurfaceTransformFlags const&,stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags const&
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* stappler::xenolith::core::SurfaceTransformFlags

# ::stappler::xenolith::core::operator^(stappler::xenolith::core::SurfaceTransformFlags const&,stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags const&
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* stappler::xenolith::core::SurfaceTransformFlags

# ::stappler::xenolith::core::operator|=(stappler::xenolith::core::SurfaceTransformFlags&,stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags&
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* stappler::xenolith::core::SurfaceTransformFlags&

# ::stappler::xenolith::core::operator&=(stappler::xenolith::core::SurfaceTransformFlags&,stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags&
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* stappler::xenolith::core::SurfaceTransformFlags&

# ::stappler::xenolith::core::operator^=(stappler::xenolith::core::SurfaceTransformFlags&,stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags&
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* stappler::xenolith::core::SurfaceTransformFlags&

# ::stappler::xenolith::core::operator==(stappler::xenolith::core::SurfaceTransformFlags const&,std::underlying_type<SurfaceTransformFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags const&
* std::underlying_type<SurfaceTransformFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator==(std::underlying_type<SurfaceTransformFlags>::type const&,stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<SurfaceTransformFlags>::type const&
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(stappler::xenolith::core::SurfaceTransformFlags const&,std::underlying_type<SurfaceTransformFlags>::type const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags const&
* std::underlying_type<SurfaceTransformFlags>::type const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator!=(std::underlying_type<SurfaceTransformFlags>::type const&,stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* std::underlying_type<SurfaceTransformFlags>::type const&
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* bool

# ::stappler::xenolith::core::operator~(stappler::xenolith::core::SurfaceTransformFlags const&)

## BRIEF

Автоматически созданный оператор битовых флагов

## CONTENT

Автоматически созданный оператор битовых флагов

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags const&

Возвращает:
* stappler::xenolith::core::SurfaceTransformFlags

# ::stappler::xenolith::core::getPureTransform(stappler::xenolith::core::SurfaceTransformFlags)

## BRIEF

Удаляет дополнительные флаги из флагов трансформации

## CONTENT

Удаляет дополнительные флаги из флагов трансформации

Параметры:
* stappler::xenolith::core::SurfaceTransformFlags

Возвращает:
* stappler::xenolith::core::SurfaceTransformFlags

# ::stappler::xenolith::core::RenderingLevel

## BRIEF

Уровень рендеринга объекта

## CONTENT

Уровень рендеринга объекта

Значения:
* Default - вычисляется приложением
* Solid - непрозрачные объекты
* Surface - прозначные объекты, находящиеся на поверхности непрозрачных
* Transparent - прочие прозрачные объекты


# ::stappler::xenolith::core::ObjectType

## BRIEF

Тип объекта графического устройства

## CONTENT

Тип объекта графического устройства

Значения:
* Unknown
* Buffer
* BufferView
* CommandPool
* DescriptorPool
* DescriptorSetLayout
* Event
* Fence
* Framebuffer
* Image
* ImageView
* Pipeline
* PipelineCache
* PipelineLayout
* QueryPool
* RenderPass
* Sampler
* Semaphore
* ShaderModule
* DeviceMemory
* Swapchain


# ::stappler::xenolith::core::PixelFormat

## BRIEF

Базовый формат пикселя

## CONTENT

Базовый формат пикселя

Значения:
* Unknown
* A
* IA
* RGB
* RGBA
* D
* DS
* S


# ::stappler::xenolith::core::ClockType

## BRIEF

Тип отсчёта времени

## CONTENT

Тип отсчёта времени

Значения:
* Default
* Monotonic - стандартные монотонные часы
* Realtime - часы реального времени
* Process - часы процесса
* Thread - часы потока
