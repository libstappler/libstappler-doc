Title: SPHalfFloat.h


# STAPPLER_CORE_UTILS_SPHALFFLOAT_H_

## BRIEF

Макрос защиты заголовка

## CONTENT

Макрос защиты заголовка

# ::stappler::halffloat::nan()

## BRIEF

Возвращает значение NaN для 16-битного значения с плавающей точкой

## CONTENT

Возвращает значение NaN для 16-битного значения с плавающей точкой согласно IEEE 754-2008

Возвращает:
* uint16_t - значение NaN (0x7e00)

# ::stappler::halffloat::posinf()

## BRIEF

Возвращает значение положительной бесконечности для 16-битного значения с плавающей точкой

## CONTENT

Возвращает значение положительной бесконечности для 16-битного значения с плавающей точкой согласно IEEE 754-2008

Возвращает:
* uint16_t - значение положительной бесконечности (31 << 10)

# ::stappler::halffloat::neginf()

## BRIEF

Возвращает значение отрицательной бесконечности для 16-битного значения с плавающей точкой

## CONTENT

Возвращает значение отрицательной бесконечности для 16-битного значения с плавающей точкой согласно IEEE 754-2008

Возвращает:
* uint16_t - значение положительной бесконечности (63 << 10)

# ::stappler::halffloat::decode(uint16_t)

## BRIEF

Декодирует 16-битное значение с плавающей точкой

## CONTENT

Декодирует 16-битное значение с плавающей точкой в 32-битное значение согласно IEEE 754-2008

Параметры:
* uint16_t - закодированное 16-битное значение

Возвращает:
* float - декодированное 32-битное значение

# ::stappler::halffloat::encode(float)

## BRIEF

Кодирует 16-битное значение с плавающей точкой

## CONTENT

Кодирует 16-битное значение с плавающей точкой из 32-битного значения согласно IEEE 754-2008

Параметры:
* float - исходное 32-битное значение

Возвращает:
* uint16_t - закодированное 16-битное значение
