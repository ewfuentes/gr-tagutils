# Copyright 2011,2012 Free Software Foundation, Inc.
#
# This file is part of GNU Radio
#
# GNU Radio is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 3, or (at your option)
# any later version.
#
# GNU Radio is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with GNU Radio; see the file COPYING.  If not, write to
# the Free Software Foundation, Inc., 51 Franklin Street,
# Boston, MA 02110-1301, USA.

########################################################################
# Install public header files
########################################################################
include(GrMiscUtils)
GR_EXPAND_X_H(tagutils tag_at_offset_XX             ss ii ff cc bb)
GR_EXPAND_X_H(tagutils tag_to_byte_Xb   s i f c b)

add_custom_target(tagutils_generated_includes DEPENDS
    ${generated_includes}
)
install(FILES
    api.h
    ${generated_sources}
    tag_thresh_switch.h
    tag_extract_cc.h DESTINATION include/tagutils
)
